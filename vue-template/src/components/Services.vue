<template>
  <div id="services">
    <div class="container">
      <h1 class="sub-title">SERVICES</h1>
      <div class="services-list">
        <div v-for="(service, index) in services" :key="index">
          <h2>{{ service.title }}</h2>
          <p>{{ service.description }}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue';
const services = ref([
  {
    title: 'UX/UI DESIGN',
    description: 'For UX/UI design services, I specialize in developing simple and straightforward digital experiences that are specific to your users\' demands. With a sharp eye for aesthetics and a focus on usability, I create interfaces that not only look good but also increase user engagement and happiness. Let\'s work together to improve your digital presence and leave a lasting impact on your audience.'
  },
  {
    title: 'GRAPHIC DESIGN',
    description: 'For graphic design services, I specialize in turning ideas into visually spectacular works that attract and inspire. Whether I\'m creating eye-catching posters, engaging social media visuals, or memorable packaging, I attempt to reflect your brand\'s essence through each design component. Let\'s work together to strengthen your brand\'s identity and stand out in today\'s competitive market.'
  },
  {
    title: 'WEB DESIGN',
    description: 'When it comes to web design services, I specialize in developing appealing online experiences that smoothly combine form and function. From easy navigation to visually appealing design, I specialize in creating websites that not only captivate your audience but also produce results. Let\'s work together to enhance your digital presence and leave a memorable impression on your visitors.'
  },
  {
    title: 'VIDEO EDITING',
    description: 'In the realm of video editing, I specialize in converting raw material into grabbing visual narratives that attract viewers. With a great eye for detail and a passion for storytelling, I bring your vision to life using smooth transitions, appealing images, and dynamic editing techniques. We can work together to bring your video projects to life, ensuring they not only meet but exceed your expectations.'
  }
]);
</script>
