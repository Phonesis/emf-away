<template>
  <div class="gaiter-card">
    <img src="../assets/gaiter-pic.jpg" alt="gaiter" class="gaiter-pic" width = "115" height = "126"/>
    <div
      class="gaiter-info"
    >
      <h2 class="gaiter-title">
        {{ productName }}
      </h2>
      <div class="gaiter-link">
        <a :href="link" class="button" target="_blank">Buy on Etsy</a>
      </div><br>
    </div>
  </div>
</template>

<script lang='ts'>
import { Component, Prop, Vue } from 'vue-property-decorator';

@Component
export default class GaiterProduct extends Vue {
    @Prop() private productName!: string;
    @Prop() private link!: string;
}
</script>

<style>
  .gaiter-card {
    z-index: 100;
    width: 50%;
    height: 30;
    display: block;
    margin-left: auto;
    margin-right: auto;
  }
  .gaiter-pic {
    z-index: 100;
    width: 50%;
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
</style>