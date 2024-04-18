<template>
  <div id="header">
    <video autoplay loop muted id="bg-video">
      <source :src="videoSource" type="video/mp4">
      Your browser does not support the video tag.
    </video>

    <div class="container">
      <nav>
        <a href="#header"><img :src="imageSrcLogo" class="logo"></a>
        <ul>
          <li><a href="javascript:void(0)" @click="scrollToTop">HOME</a></li>
          <li><a href="#about">ABOUT</a></li>
          <li><a href="#services">SERVICES</a></li>
          <li><a href="#portfolio">PORTFOLIO</a></li>
          <li><a href="#contact">CONTACT</a></li>
        </ul>
      </nav>

      <div class="header-text">
        <h1>HI, I AM<span> SALI </span> <br> AND I AM A MULTIMEDIA DESIGNER </h1>
      </div>
    </div>
  </div>
</template>

<script setup>

import { ref } from 'vue';
import imageSrc61 from '@/assets/images/6.1.png';
import videoSrc from '@/assets/videos/video2.mp4';

const imageSrcLogo = ref(imageSrc61);
const videoSource = ref(videoSrc); 

const scrollToTop = () => {
  window.scrollTo({ top: 0, behavior: 'smooth' });
};

</script>
