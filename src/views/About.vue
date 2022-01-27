<template>
  <div class="about">
    <main>
      <img :src="image" alt="EMF-Away"/><br><br>
      <img class="profile-pic" :src="profileImage" alt="Profile Pic"/><br>
      <h1>My name is Julia and I create EMF protective clothing :) I am a fiber artist and Textile Designer/maker, based in South of England. 💜☀️</h1>
      <a href="https://twitter.com/missjulia_ann" target="_blank">Follow me on Twitter</a><br><br><br>
    </main>
  </div>

</template>

<script>
  import image from "../assets/logo-emf.jpg"
  import profileImage from "../assets/profile-pic.jpg"

  export default {
    name: 'App',
    data () {
      return {
        image: image,
        profileImage: profileImage
      }
    },
  }
</script>

<style>
  h1 {
    font-style: italic;
    font-size: medium;
    font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
  }
  .profile-pic {
    display: block;
    position: left;
    margin-right: auto;
    padding: 2px;
    width: 150px;
    left: 80%;
    border-radius: 50%;
  }
</style>
