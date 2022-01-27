<template>
  <div class="sock-card">
    <img src="../assets/sock-pic.png" alt="sock" class="sock-pic" width = "115" height = "126"/>
    <div
      class="sock-info"
    >
      <h2 class="sock-title">
        {{ productName }}
      </h2>
      <slot></slot>
      <div class="sock-link">
        <a :href="link" class="button" target="_blank">Buy on Etsy</a>
      </div><br>
    </div>
  </div>
</template>

<script lang='ts'>
import { Component, Prop, Vue } from 'vue-property-decorator';

@Component
export default class SockProduct extends Vue {
    @Prop() private productName!: string;
    @Prop() private link!: string;
}
</script>

<style>
  .sock-card {
    z-index: 100;
    width: 50%;
    height: 30;
    display: block;
    margin-left: auto;
    margin-right: auto;
  }
  .sock-pic {
    z-index: 100;
    width: 50%;
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
</style>