<template>
  <div class="about">
    <main>
      <br><img class="profile-pic" :src="profileImage" alt="Profile Pic"/><br><br>
      <h1>My name is Julia and I create protective silver based clothing to help shield you against harmful EMFs (Electric & Magnetic Fields) <br> <br> I am a fiber artist and textile designer/maker, based in the South of England. 💜☀️</h1><br>
      <img class="mail-icon" :src="mailIcon" alt="Mail"/>
      <a href="mailto:emf-away@hotmail.com?subject=EMF Away query">Got a query, email me</a><br><br><br>
    </main>
  </div>

</template>

<script>
  import image from "../assets/logo-emf.jpg"
  import profileImage from "../assets/profile-pic.jpg"
  import twitterPic from "../assets/twitter-logo.png"
  import mailIcon from "../assets/mail-icon.png"

  export default {
    name: 'App',
    data () {
      return {
        image: image,
        profileImage: profileImage,
        twitterPic: twitterPic,
        mailIcon: mailIcon
      }
    },
  }
</script>

<style>
  h1 {
    font-size: medium;
    color: #302e86;
    font-family: Arial, Helvetica, sans-serif
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
  .twitter-pic, .mail-icon {
    width: 50px;
  }
</style>
