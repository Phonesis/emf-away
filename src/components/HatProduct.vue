<template>
  <div class="hat-card">
    <img src="../assets/hat-pic.jpg" alt="hat" class="hat-pic" width = "115" height = "126"/>
    <div
      class="hat-info"
    >
      <h2 class="hat-title">
        {{ productName }}
      </h2>
      <slot></slot>
      <div class="hat-link">
        <a :href="link" class="button" target="_blank">Buy on Etsy</a>
      </div><br>
    </div>
  </div>
</template>

<script lang='ts'>
import { Component, Prop, Vue } from 'vue-property-decorator';

@Component
export default class HatProduct extends Vue {
    @Prop() private productName!: string;
    @Prop() private link!: string;
}
</script>

<style>
  .hat-card {
    z-index: 100;
    width: 50%;
    height: 30;
    display: block;
    margin-left: auto;
    margin-right: auto;
  }
  .hat-pic {
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