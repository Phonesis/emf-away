<template>
  <div id="app">
    <main>
      <img :src="image" alt="EMF-Away"/><br>
      <a href="https://www.etsy.com/uk/shop/EMFAWAY" target="_blank">View my Etsy Store</a><br>
      <h2>I create EMF protective clothing to help protect you and your family. Here are my latest offerings available to buy on Etsy:</h2><br>
      <div class="grid-container">
        <div class="grid-item"> 
          <HatProduct 
            productName="Silver EMF Protective Hat/Beanie" 
            link="https://www.etsy.com/uk/listing/1070907542/silver-emf-protective-hat?click_key=68580ea1f31826d3efe634c8a28f8f63f8ea3344%3A1070907542&click_sum=ec70b4d0&ref=shop_home_active_1&frs=1&sca=1"
          />
          <h3>This is a hat designed to be worn under any other hats. It is pure silver coated fabric that has a shielding efficiency of >55DB or more.<br><br> It is EMF shielding and also has anti bacterial, conductive, healing and anti-radiation functions, which can help protect against 5G.</h3>
        </div>
        <div class="grid-item"> 
          <GaiterProduct 
            productName="Silver EMF Protective Gaiter" 
            link="https://www.etsy.com/uk/listing/1108536877/silver-emf-protective-gaiter?click_key=3d95a2e07a3b2e28930259690037a5537ba90dfc%3A1108536877&click_sum=67a3754a&ref=shop_home_recs_2&frs=1&sca=1"
          />
        <h3>This Silver snood will keep those EMFs away this winter whilst protecting your Thyroid and keeping your neck warm 😊 <br><br> We love this Silver snood 💞 the larger fit, can also be worn over face- if necessary and over the head. Multi purpose. Fabric is anti-viral and Anti-bacterial and helps with circulation not to mention how pretty it makes anyone look 💜
        Team it with a Shungite or Orgone pendant for extra protection 💕</h3>
        </div>
        <div class="grid-item"> 
          <SockProduct 
            productName="Silver Fibre Grounding Socks" 
            link="https://www.etsy.com/uk/listing/1108605007/26-pure-silver-fibre-grounding-socks?click_key=582545ea6ea46a19e0dd1179b5460806a2de0d95%3A1108605007&click_sum=7f701372&ref=shop_home_recs_3&frs=1&cns=1"
          />
        <h3>I have been very fortunate to obtain a small stock of Grounding socks. <br> <br> Grounding in nature is essential for our wellbeing and health. Also known as earthing, allows you to channel the earths natural energy through direct bodily contact with earths surface and replenish diminished electrons.</h3>
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

  export default {
    name: 'App',
    components:{
      HatProduct,
      GaiterProduct,
      SockProduct
    },
    data () {
      return {
        image: image,
      }
    },
  }
</script>

<style>
  * {
    padding: 0;
    text-align: center;
  }

  img {
    display: block;
    margin-left: auto;
    margin-right: auto;
    padding: 2px;
    width: 250px;
    border-radius: 50%;
  }

  .grid-container {
    display: inline-grid;
    grid-template-columns: auto auto auto;
    background-color: #95adc0;
    padding: 3px;
  }
  .grid-item {
    background-color: rgba(255, 255, 255, 0.8);
    border: 1px solid rgba(0, 0, 0, 0.8);
    padding: 30px;
    font-size: 30px;
    text-align: center;
    position:relative;
  }

  a {
    font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
    position: relative;
    text-align: center;
    font-style:inherit;
    font-size: 5;
  }

  h1 {
    position: relative;
    text-align: center;
    font-style:inherit;
    font-size: 5;
    font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
  }

  h2 {
    font-style: italic;
    font-size: medium;
    font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
  }

  h3 {
    font-size: small;
    text-align:justify;
    right:30%;
    top:20px;
    left: 30%;
    font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
  }

  body {
    font-family: sans-serif;
  }

  #app {
    background-color: rgb(160, 189, 179);
    background-size:auto
  }
</style>
