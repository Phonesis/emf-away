<template>
  <div class="hat-card">
    <img src="../assets/hat-pic.jpg" alt="hat" class="hat-pic" width = "150" height = "200"/>
    <div
      class="hat-info"
    ><br>
      <h2 class="hat-title">
        {{ productName }}
      </h2>
      <h2 class="hat-price">
        {{ price }}
      </h2><br>
      <div class="container">
        <div class="overlay"></div>
        <div class="hat-link">
          <a :href="link" class="button" title="View product on Etsy" target="_blank">Buy on Etsy</a>
        </div><br>
      </div>
    </div>
  </div>
</template>

<script lang='ts'>
import { Component, Prop, Vue } from 'vue-property-decorator';

@Component
export default class HatProduct extends Vue {
    @Prop() private productName!: string;
    @Prop() private link!: string;
    @Prop() private price!: string;
}
</script>

<style>
  .hat-card {
    z-index: 100;
    height: 30;
    display: block;
    margin-left: auto;
    margin-right: auto;
  }
  .hat-pic {
    z-index: 100;
    border: 5px solid #555;
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
  }
  h2 {
    width: 100%;
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
</style>