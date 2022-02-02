<template>
  <div id="app">
    <br><img class="logo" :src="image" alt="EMF-Away"/>
    <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link> |
      <a href="https://www.etsy.com/uk/shop/EMFAWAY" title="View my Etsy Store" target="_blank">Etsy Store</a><br>
    </div>
  <transition name="fade">
    <router-view></router-view>
  </transition>
  </div>
</template>

<script>
  import image from "./assets/logo-emf.jpg"

  export default {
    name: 'App',
    data () {
      return {
        image: image,
      }
    },
  }
</script>


<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #302e86;
}

img {
  display: block;
  margin-left: auto;
  margin-right: auto;
  padding: 2px;
  width: 250px;
  border-radius: 10%;
}

#nav {
  padding: 30px;
  color: #302e86;
}

#nav a {
  font-weight: bold;
  color: #302e86;
}

#nav a.router-link-exact-active {
  color: green
}

.fade-enter-active, .fade-leave-active {
  transition-property: opacity;
  transition-duration: .25s;
}

.fade-enter-active {
  transition-delay: .25s;
}

.fade-enter, .fade-leave-active {
  opacity: 0
}

</style>
