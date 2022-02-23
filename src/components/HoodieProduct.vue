<template>
  <div class="hoodie-card">
    <img src="../assets/hoodie-pic.jpg" alt="hoodie" class="hoodie-pic" width = "150" height = "200"/>
    <div
      class="hoodie-info"
    ><br>
      <h2 class="hoodie-title">
        {{ productName }}
      </h2>
      <h2 class="hoodie-price">
        {{ price }}
      </h2><br>
      <div class="container">
        <div class="overlay"></div>
        <div class="hoodie-link">
          <a :href="link" class="button" title="View product on Etsy" target="_blank">Buy on Etsy</a>
        </div><br>
      </div>
    </div>
  </div>
</template>

<script lang='ts'>
import { Component, Prop, Vue } from 'vue-property-decorator';

@Component
export default class HoodieProduct extends Vue {
    @Prop() private productName!: string;
    @Prop() private link!: string;
    @Prop() private price!: string;
}
</script>

<style>
  .hoodie-card {
    z-index: 100;
    height: 30;
    display: block;
    margin-left: auto;
    margin-right: auto;
  }
  .hoodie-pic {
    z-index: 100;
    border: 5px solid #555;
  }
  .button {
    background-color: #4CAF50;
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