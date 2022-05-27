<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
   name: 'navbar',
   setup() {
      return {};
   },
});
</script>

<template>
   <nav class="navbar sticky-top navbar-expand-lg bg-light">
      <div class="container">
         <button
            class="navbar-toggler"
            type="button"
            data-bs-toggle="collapse"
            data-bs-target="#navbarSupportedContent"
            aria-controls="navbarSupportedContent"
            aria-expanded="false"
            aria-label="Toggle navigation"
         >
            <span class="navbar-toggler-icon"></span>
         </button>
         <div class="collapse navbar-collapse" id="navbarSupportedContent">
            <ul class="navbar-nav me-auto mb-2 mb-lg-0">
               <li class="nav-item">
                  <a class="nav-link" aria-current="page" href="#">Home</a>
               </li>
               <li class="nav-item">
                  <a class="nav-link" href="#about-section">About</a>
               </li>
               <li class="nav-item">
                  <a class="nav-link" href="#projects-section">Projects</a>
               </li>
            </ul>
            <a
               href="https://drive.google.com/file/d/1WfOEXNGdyHr3LP-Bkqb-xHzl-NFg2a2o/view?usp=sharing"
               target="_blank"
            >
               <button
                  type="button"
                  class="primary-btn btn btn-outline-dark"
                  style="border-radius: 20px"
               >
                  Download CV
               </button>
            </a>
         </div>
      </div>
   </nav>
</template>

<style lang="scss" scoped>
nav {
   background-color: #17213c !important;
   color: white !important;

   .nav-link {
      color: white !important;
   }

   .nav-link:hover {
      color: #ff5004 !important;
   }
}
</style>


