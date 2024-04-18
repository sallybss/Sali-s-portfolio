<template>
  <footer>
    <div class="container">
      <div class="footer-content">
        <a href="#header"><img :src="imageSrcLogo" class="footer-logo" alt="Footer Logo"></a>
        <div class="footer-left">
          <p>Email: salinkaaa36@gmail.com</p>
          <p>Phone: +45 53 35 01 31</p>
        </div>
        <div class="footer-right">
          <a href="https://www.linkedin.com/in/sali-bseso-452735293/" target="_blank">
            <img :src="imageSrcLinkedIn" alt="LinkedIn" width="30" height="30">
          </a>
        </div>
      </div>
      <div class="copyright">
        <p>&copy; 2024 Sali. All rights reserved.</p>
      </div>
    </div>
  </footer>
</template>

<script setup>
import imageSrcLogo from '@/assets/images/6.1.png'; 
import imageSrcLinkedIn from '@/assets/images/linkedin.png'; 
</script>