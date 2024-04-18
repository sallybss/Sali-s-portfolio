<template>
  <div id="about">
    <div class="container">
      <div class="row">
        <div class="about-col-1">
          <img :src="imageSrcAbout" alt="About Image">
        </div>
        <div class="about-col-2">
          <h1 class="sub-title">ABOUT ME</h1>
          <p>{{ aboutContent }}</p>
          <div class="tab-titles">
            <p class="tab-links" :class="{ 'active-link': activeTab === 'CV' }" @click="activeTab = 'CV'">CV</p>
            <p class="tab-links" :class="{ 'active-link': activeTab === 'education' }" @click="activeTab = 'education'">Education</p>
          </div>
      
          <div v-if="activeTab === 'education'" class="tab-contents active-tab">
            <ul>
              <li v-for="(item, index) in educationContent" :key="index">
                <span>{{ item.title }}</span><br>{{ item.description }}
              </li>
            </ul>
          </div>

          <div v-if="activeTab === 'CV'" class="tab-contents active-tab">
            <div class="video-container">
              <iframe class="video-frame" :src="videoSrc" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe> </div>
            <a :href="cvPDF" download="CV-sali.pdf" class="btn btn2">Download CV</a>
          </div>
        </div>
      </div>
    </div>

    <div class="container">
      <img :src="skills" alt="Additional Image" class="additional-image">
    </div>

  </div>
</template>

<script setup>
import { ref } from 'vue';
import imageSrcAbout from '@/assets/images/IMG_3628.pngda.png';
import cvPDF from '@/assets/images/CV-sali.pdf';
import skills from '@/assets/images/skills.png';

const activeTab = ref('CV');
const aboutContent = ref(`
  Welcome to my portfolio! I'm Sali, a multimedia designer originally from Bulgaria and now based in Denmark. With an ambitious nature and a creative mindset, I'm deeply passionate about designing various projects. Currently pursuing my studies in Multimedia Design at BASW Esbjerg, I've already gained valuable skills and insights. I thrive on merging creativity with practicality to develop products that not only look visually appealing but also ensure exceptional user experiences. Beyond design, I enjoy spending time outdoors with friends or in nature. Eager for new projects and collaborations, let's join forces to craft something truly remarkable together!
`);
const educationContent = ref([
  {
    title: 'MULTIMEDIA DESIGN 2023 - PRESENT',
    description: `I'm presently enrolled in a multimedia design programme in BASW/EASV Denmark, where the curriculum covers a wide range of competencies and resources necessary for working in the field. I have developed a solid understanding of programming, using tools like HTML, CSS, and JS. Through this education journey, I have gained proficiency in Adobe software, including Illustrator, Adobe XD, Photoshop, InDesign, Premiere Pro, and After Effects.`
  }
]);
const videoSrc = 'https://www.youtube.com/embed/d2gkyfd1yFk?si=puOR9i7C8w5kbT8i';
</script>
