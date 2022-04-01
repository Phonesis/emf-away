<template>
  <div id="app">
    <main>
      <h4>I create clothing designed to help protect you and your family against the potentially harmful effects of EMF (Electric & Magnetic Fields) exposure. <br> <br> Here are some of my latest offerings available to buy on Etsy (links will open in a new tab):</h4><br>
      <div v-if="!isMobile()">
        <div class="grid-container">
          <div class="grid-item"> 
            <HatProduct 
              productName="Silver EMF Protective Hat/Beanie" 
              price="£39 / $52" 
              link="https://www.etsy.com/uk/listing/1070907542/silver-emf-protective-hat?click_key=68580ea1f31826d3efe634c8a28f8f63f8ea3344%3A1070907542&click_sum=ec70b4d0&ref=shop_home_active_1&frs=1&sca=1"
            />
            <h3>This is a hat designed to be worn under any other hats. It is pure silver coated fabric that has a shielding efficiency of >55DB or more.<br><br> It is EMF shielding and also has anti bacterial, conductive, healing and anti-radiation functions, which can help protect against 5G.</h3>
          </div>
          <div class="grid-item"> 
            <GaiterProduct 
              productName="Silver EMF Protective Gaiter" 
              price="£29 / $38" 
              link="https://www.etsy.com/uk/listing/1108536877/silver-emf-protective-gaiter?click_key=3d95a2e07a3b2e28930259690037a5537ba90dfc%3A1108536877&click_sum=67a3754a&ref=shop_home_recs_2&frs=1&sca=1"
            />
          <h3>This Multi purpose silver snood will keep those EMFs away this winter whilst protecting your Thyroid and keeping your neck warm. <br><br> We love this Silver snood. The larger fit can also be worn over your face if necessary and even over the head. Fabric is anti-viral and Anti-bacterial and helps with circulation not to mention how pretty it makes anyone look!</h3>
          </div>
          <div class="grid-item"> 
            <SockProduct 
              productName="Silver Fibre Grounding Socks" 
              price="£24 / $32" 
              link="https://www.etsy.com/uk/listing/1108605007/26-pure-silver-fibre-grounding-socks?click_key=582545ea6ea46a19e0dd1179b5460806a2de0d95%3A1108605007&click_sum=7f701372&ref=shop_home_recs_3&frs=1&cns=1"
            />
          <h3>I have been very fortunate to obtain a small stock of Grounding socks. <br> <br> Grounding in nature is essential for our wellbeing and health. Also known as earthing, it allows you to channel natural energy through direct bodily contact with the planet surface and helps replenish diminished electrons.</h3>
          </div>
          <div class="grid-item"> 
            <HoodieProduct Zip
              productName="Ladies EMF Protective Hoodie" 
              price="£145 / $196" 
              link="https://www.etsy.com/uk/listing/1173926627/ladies-emf-protective-black-zip-hoodie?click_key=f1665214fac158dcc590965e0c71e775e040c586%3A1173926627&click_sum=97c7b758&ref=shop_home_recs_4"
            />
          <h3>EMF protective armour. Black and silver multilayered knit hoodie. Will protect from all EMFs.<br><br> Comfortable, looks good, and will keep you protected.<br></h3>
          </div>
        </div>
      </div>
      <div v-else>
        <div class="grid-container-mob">
          <div class="grid-item-mob"> 
            <HatProduct 
              productName="Silver EMF Protective Hat/Beanie" 
              price="£39 / $52" 
              link="https://www.etsy.com/uk/listing/1070907542/silver-emf-protective-hat?click_key=68580ea1f31826d3efe634c8a28f8f63f8ea3344%3A1070907542&click_sum=ec70b4d0&ref=shop_home_active_1&frs=1&sca=1"
            />
            <h3>This is a hat designed to be worn under any other hats. It is pure silver coated fabric that has a shielding efficiency of >55DB or more.<br><br> It is EMF shielding and also has anti bacterial, conductive, healing and anti-radiation functions, which can help protect against 5G.</h3>
          </div>
          <div class="grid-item-mob"> 
            <GaiterProduct 
              productName="Silver EMF Protective Gaiter" 
              price="£29 / $38" 
              link="https://www.etsy.com/uk/listing/1108536877/silver-emf-protective-gaiter?click_key=3d95a2e07a3b2e28930259690037a5537ba90dfc%3A1108536877&click_sum=67a3754a&ref=shop_home_recs_2&frs=1&sca=1"
            />
          <h3>This Multi purpose silver snood will keep those EMFs away this winter whilst protecting your Thyroid and keeping your neck warm. <br><br> We love this Silver snood. The larger fit can also be worn over your face if necessary and even over the head. Fabric is anti-viral and Anti-bacterial and helps with circulation not to mention how pretty it makes anyone look!</h3>
          </div>
          <div class="grid-item-mob"> 
            <SockProduct 
              productName="Silver Fibre Grounding Socks" 
              price="£24 / $32" 
              link="https://www.etsy.com/uk/listing/1108605007/26-pure-silver-fibre-grounding-socks?click_key=582545ea6ea46a19e0dd1179b5460806a2de0d95%3A1108605007&click_sum=7f701372&ref=shop_home_recs_3&frs=1&cns=1"
            />
          <h3>I have been very fortunate to obtain a small stock of Grounding socks. <br> <br> Grounding in nature is essential for our wellbeing and health. Also known as earthing, it allows you to channel natural energy through direct bodily contact with the planet surface and helps replenish diminished electrons.</h3>
          </div>
          <div class="grid-item-mob"> 
            <HoodieProduct 
              productName="Ladies EMF Protective Hoodie" 
              price="£145 / $196" 
              link="https://www.etsy.com/uk/listing/1173926627/ladies-emf-protective-black-zip-hoodie?click_key=f1665214fac158dcc590965e0c71e775e040c586%3A1173926627&click_sum=97c7b758&ref=shop_home_recs_4"
            />
          <h3>EMF protective armour. Black and silver multilayered knit hoodie. Will protect from all EMFs.<br><br> Comfortable, looks good, and will keep you protected.<br></h3>
          </div>
        </div>
      </div>
    </main>
  </div>
</template>

<script>
  import image from "../assets/logo-emf.jpg"
  import HatProduct from '../components/HatProduct.vue'
  import GaiterProduct from '../components/GaiterProduct.vue'
  import SockProduct from '../components/SockProduct.vue'
  import HoodieProduct from '../components/HoodieProduct.vue'

  export default {
    name: 'App',
    components:{
      HatProduct,
      GaiterProduct,
      SockProduct,
      HoodieProduct
    },
    data () {
      return {
        image: image,
      }
    },
    methods: {
      isMobile() {
        if(/Android|webOS|iPhone|iPad|iPod|BlackBerry|IEMobile|Opera Mini/i.test(navigator.userAgent)) {
          return true
        } else {
          return false
        }
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
    padding: 3px;
  }
  .grid-item {
    background-color: #302e86;
    border: 1px solid rgba(0, 0, 0, 0.8);
    padding: 30px;
    font-size: 30px;
    text-align: center;
    position:relative;
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
