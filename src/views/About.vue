<template>
  <div class="about">
    <main>
      <br><img class="profile-pic" :src="profileImage" alt="Profile Pic"/><br><br>
      <h1>My name is Julia and I create protective silver based clothing to help shield you against harmful EMFs (Electric & Magnetic Fields) <br> <br> I am a fiber artist and textile designer/maker, based in the South of England. 💜☀️</h1><br><br>
      <img class="mail-icon" :src="mailIcon" alt="Mail"/>
      <a href="mailto:emf-away@hotmail.com?subject=EMF Away query">Got a query? Drop me an email</a><br><br>
      <img class="twitter-pic" :src="twitterPic" alt="Twitter"/>
      <a href="https://twitter.com/missjulia_ann" target="_blank">Follow me on Twitter</a><br><br><br><br>
      <h1>Some interesting links regarding EMF and 5G:</h1><br><br>
      <iframe width="420" height="315"
      src="https://www.youtube.com/embed/SOhbKSe1ecQ">
      </iframe><br><br><br>
      <a href="https://actionagainst5g.org/legal-case/"> 5G Legal Case by Michael Mansfield QC</a><br><br><br><br>
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
    color: beige;
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
  #html {
    background-color: rgb(3, 3, 3);
  }
</style>
