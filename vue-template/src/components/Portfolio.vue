<template>
  <div id="portfolio">
    <div class="container">
      <h1 class="sub-title">PROJECTS</h1>
      <div class="work-container">
        <div class="work-list">
          <div class="work" v-for="(item, index) in portfolioItems" :key="index">
            <img :src="item.image" :alt="item.title">
            <div class="layer">
              <h3>{{ item.title }}</h3>
              <p>{{ item.description }}</p>
              <a v-if="index === 0" :href="item.link1" target="_blank">More</a>
              <a v-else-if="index === 3" :href="item.link2" target="_blank">More</a>
              <a v-else-if="index === 4" :href="item.link3" target="_blank">More</a>
              <a v-else-if="index === 6" :href="item.link4" target="_blank">More</a>
              <a v-else-if="index === 7" :href="item.link5" target="_blank">More</a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue';
import podcast from '@/assets/images/mockups3.png';
import merch from '@/assets/images/merch.png';
import videoedit from '@/assets/images/video editing.png';
import webdesign from '@/assets/images/webdesign.png';
import studentMerch from '@/assets/images/student merch.png';
import bcards from '@/assets/images/bcards.png';
import foodApp from '@/assets/images/foodapp.png';
import logodesign from '@/assets/images/logo.png';
import podcastPDF from '@/assets/images/podcast.pdf';

const portfolioItems = ref([
  {
    title: "PODCAST APP",
    description: "Introducing the Trapholt Museum Podcast App! Dive into educational fun with a simple, Spotify-inspired interface. Explore exhibitions, architects, and designers in vibrant stories about art, architecture, and design—an essential resource for students and teachers alike!",
    image: podcast,
    link1: podcastPDF,
  },
  {
    title: "LOGO DESIGN",
    description: "Elevate your brand with my captivating logo designs. Crafted with precision and creativity, each design embodies your brand's essence, leaving a lasting impression on your audience. Let me tell your brand's story through my distinctive designs, ensuring your identity shines through in every detail.",
    image: logodesign,
  },
  {
    title: "MERCHANDISE",
    description: "Introducing my personalized clothing service! Elevate your style with custom designs tailored just for you. Whether it's a special message, artwork, or favorite colors, my creations reflect your individuality while promoting sustainability and art appreciation. Plus, add a personalized name logo to make it truly yours.",
    image: merch,
  },
  {
    title: "THE STALKER",
    description: "During a workshop on video production at my current academy, I created 'The Stalker' as part of honing my skills in video editing using Premiere Pro and After Effects. This hands-on experience provided access to professional materials and a dedicated green screen room, allowing me to refine my craft with practical application.",
    image: videoedit,
    link2: 'https://youtu.be/loWjnHSSwnw',
  },
  {
    title: "WEB DESIGN",
    description: "I've crafted a website design for a brand I conceptualized called Organish, specializing in natural hair oils. The design features a neutral color palette and comprises a one-page application with five sections. Using Adobe XD, I've created a mockup that embodies the essence of the brand and its commitment to organic hair care.",
    image: webdesign,
    link3: 'https://xd.adobe.com/view/2c97a3ca-8ead-4346-83d9-312f956aa79b-79c4/',
  },
  {
    title: "STUDENT MERCHANDISE",
    description: "Introducing our student merchandise line at Trapholt Museum! Eco-friendly tote bags feature our logo and Nanna Ditzel's 'Bench for Two' illustration, while student passes showcase designs inspired by Ditzel's ND83 chair. Both items reinforce our commitment to creativity, education, and sustainability in art.",
    image: studentMerch,
  },
  {
    title: "BUSINESS CARD",
    description: "I've designed my own business card using Adobe Illustrator. One side features my personal Chrometype 3D logo made with Adobe Dimension, while the other side includes two QR codes: one linking to my LinkedIn profile and the other to my portfolio website. Additionally, you'll find my mobile number below for easy contact.",
    image: bcards,
    link4: bcards,
  },
  {
    title: "FOOD APP",
    description: "During Sustainability Week at my academy, our group created an app mockup for the canteen to reduce food waste. The app lets users access leftover food for a cheaper price or even for free, and they can also purchase leftover food to take home. The school provides reusable boxes for this purpose.",
    image: foodApp,
    link5: foodApp,
  },
]);
</script>
