<template>
  <div id="app">
    <main>
      <h4>I create clothing designed to help protect you and your family against the potentially harmful effects of EMF (Electric & Magnetic Fields) exposure. <br> <br> Here are some of my latest creations available to buy via my store or through Etsy (links will open in a new tab):</h4><br>
      <div class="cart">
        <div>Items in Cart: {{cart.length}}</div>
        <div>Total: £{{ cart.reduce((totalPrice, item) => totalPrice + item.price, 0 ).toFixed(2)}}</div>
        <button @click="refreshCart()">Refresh Cart</button>
        <h4>Checkout</h4><br>
      </div>
      <div class="grid-container">
        <h3 class="grid-item" v-for="item in items" :key="item.id">
          <img :src="getImgUrl(item.picName)" v-bind:alt=item.picName class="pic" width = "150" height = "200"/><br>
          <h2>{{ item.name }} - {{ '£' + item.price }}</h2> <br>
          <h3>{{ item.description }}</h3><br>
          <div v-if="item.shortName === 'socks'"><br></div>
          <div v-if="item.shortName === 'hoodie'"><br><br></div>
          <h5 class="inner-grid-item">
            <h5 class ="sizes">
              <h3>Size Options:</h3><br>
                <div v-if="item.shortName !== 'socks'">
                  <h2>Small</h2><button class="clickable" @click="addToCart(item, 'small')">Add to Cart</button>
                  <br><br><h2>Medium</h2><button class="clickable" @click="addToCart(item, 'medium')">Add to Cart</button>
                  <br><br><h2>Large</h2><button class="clickable" @click="addToCart(item, 'large')">Add to Cart</button><br>
                </div>
                <div v-else>
                  <h2>Standard</h2><button class="clickable" @click="addToCart(item, 'standard')">Add to Cart</button>
                </div>
              <br>
              <h2>Or</h2>
              <div class="container">
                  <div class="sock-link">
                    <a href="http://www.google.com" class="button" title="View product on Etsy" target="_blank">Buy on Etsy</a>
                </div><br>
              </div>
            </h5>
          </h5>
        </h3>
      </div>
    </main>
  </div>
</template>

<script>
  import image from "../assets/logo-emf.jpg"
  export default {
    name: 'App',
    components:{
    },
    data () {
      return {
        image: image,
         items: [
        { id: 1, shortName: 'hat', name: 'Silver EMF Protective Hat/Beanie', picName: 'hat-pic.jpg', price: 9.99, description: 'This is a hat designed to be worn under any other hats. It is pure silver coated fabric that has a shielding efficiency of >55DB or more. It is EMF shielding and also has anti bacterial, conductive, healing and anti-radiation functions, which can help protect against 5G', size: ''},
        { id: 2, shortName: 'socks', name: 'Silver Fibre Grounding Socks', picName: 'sock-pic.png', price: 19.99, description: 'I have been very fortunate to obtain a small stock of Grounding socks. Grounding in nature is essential for our wellbeing and health. Also known as earthing, it allows you to channel natural energy through direct bodily contact with the planet surface and helps replenish diminished electrons', size: '' },
        { id: 3, shortName: 'hoodie', name: 'Ladies EMF Protective Hoodie', picName: 'hoodie-pic.jpg', price: 29.99, description: 'EMF protective armour. Black and silver multilayered knit hoodie. Will protect from all EMFs. Comfortable, looks good, and will keep you protected.', size: '' },
        { id: 4, shortName: 'gaiter', name: 'Silver EMF Protective Gaiter', picName: 'gaiter-pic.jpg', price: 29.99, description: 'This Multi purpose silver snood will keep those EMFs away this winter whilst protecting your Thyroid and keeping your neck warm. The larger fit can also be worn over your face if necessary and even over the head. Fabric is anti-viral and Anti-bacterial and helps with circulation not to mention how pretty it makes anyone look!', size: '' },
        ],
        cart: []
      }
    },
    created() {
      let cart = localStorage.getItem('cart');
      if (cart) {
          try {
              this.cart = JSON.parse(cart);
          } catch (error) {
              console.error(error);
              this.cart = [];
          }
      } else {
          this.cart = [];
      }
    },
    methods: {
      isMobile() {
        if(/Android|webOS|iPhone|iPad|iPod|BlackBerry|IEMobile|Opera Mini/i.test(navigator.userAgent)) {
          return true
        } else {
          return false
        }
      },
      addToCart(product, size) {
        console.log('added ' + product.name + ' with size ' + size)
        product.size = size
        this.cart.push(product)
        localStorage.setItem('cart',  JSON.stringify(this.cart))
      },
      refreshCart() {
        console.log('refreshed')
        this.cart = []
        window.localStorage.setItem('cart', [])
      },
      getImgUrl(pic) {
        return require('../assets/'+ pic)
      }
    } 
  }
</script>

<style>
  * {
    padding: 0;
    margin: 0;
    text-align: center;
  }

  .grid-container {
    display: grid;
    grid-template-columns:auto auto auto auto;
    background-color: #95c099;
    padding: 0px;
    z-index: 1;
  }
  .grid-item {
    background-color: #302e86;
    border: 1px solid rgba(0, 0, 0, 0.8);
    padding: 30px;
    font-size: 30px;
    text-align: center;
    z-index: 1;
  }
  .inner-grid-item {
    bottom: 0;
  }
  .sizes {
    background-color: #302e86;
    border: 1px solid rgba(0, 0, 0, 0.8);
    padding: 30px;
    font-size: 30px;
    text-align: center;
    z-index: 1;
  }
  .clickable {
    z-index: 999;
  }
  .overlay {
    position: absolute;
    top: 0;
    bottom: 0;
    left: 0;
    right: 0;
    height: 100%;
    width: 100%;
    opacity: 0;
    transition: .5s ease;
    background-color: #a9b5b9;
  }

  @media only screen and (max-width: 1400px) {
    .grid-container {
      grid-template-columns: auto auto;
    }
  }

    @media only screen and (max-width: 700px) {
    .grid-container {
      grid-template-columns: auto;
    }
  }

  @media (min-width:1500px) { 
    .grid-item {
      height: 45vw;
    }
  }

  .grid-container-mob {
    display: grid;
    background-color: #95c099;
    padding: 3px;
    box-sizing: border-box;
    width: 100%;
  }
  .grid-item-mob {
    background-color: #302e86;
    border: 1px solid rgba(0, 0, 0, 0.8);
    box-sizing: border-box;
    padding: 10px;
    font-size: 30px;
    width: 100%;
    text-align: center;
    position:relative;
  }

  .button {
    background-color: #4CAF50;
    border: none;
    color: white;
    padding: 15px 32px;
    text-align: center;
    text-decoration: none;
    display: inline-block;
    font-size: 16px;
    z-index: 0;
  }

  a {
    font-family: Avenir, Helvetica, Arial, sans-serif; position: relative;
    text-align: center;
    font-style:inherit;
    font-size: 18px;
    color: #302e86;
    font-weight: bold;
  }

  h1 {
    position: relative;
    text-align: center;
    font-style:inherit;
    font-size: 5;
    font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
  }

  h2 {
    font-size: medium;
    color: beige;
    font-family: Avenir, Helvetica, Arial, sans-serif; position: relative;
  }

  h3 {
    font-size: small;
    text-align:justify;
    right:30%;
    top:20px;
    left: 30%;
    color: beige;
    font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
  }

  h4 {
    font-size: medium;
    color: #302e86;
    font-family: Avenir, Helvetica, Arial, sans-serif; position: relative;
  }

  h5 {
    position: relative;
  }

  @media (min-width:700px) { 
    .cart {
      padding: 5px;
      overflow: hidden;
      -webkit-font-smoothing: antialiased;
      -moz-osx-font-smoothing: grayscale;
      background-color:  rgb(214, 205, 205);
      position: fixed;
      top: 15%;
      right: 5%;
      width: 15%;
      opacity: 80%;
      transition: .10s ease;
      z-index: 1000;
      border-radius: 10%;
    }
  }

  body {
    font-family: sans-serif;
  }

  .logo:hover {
    border-radius:30%;
    opacity: 0.2;
  }

  #app {
    background-color: rgb(214, 205, 205);
    background-size:auto;
  }
</style>
