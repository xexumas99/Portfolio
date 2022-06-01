<script lang="ts">
import { computed } from '@vue/runtime-core';
export default {
   setup() {
      const isSmallScreen = computed(() => {
         return window.innerWidth < 480;
      });
      return { isSmallScreen };
   },
};
</script>

<template>
   <footer class="bg-dark text-center text-white">
      <div class="container py-4">
         <div class="row">
            <div
               class="col-md-6 col-xs-12"
               :style="isSmallScreen ? 'padding-top: 1em' : 'padding-top: 2em'"
            >
               <section
                  :class="isSmallScreen ? 'text-center' : 'text-start'"
                  class="mb-4"
               >
                  <a
                     class="primary-btn btn btn-outline-light btn-floating m-1"
                     href="https://twitter.com/FranMasLledo99"
                     target="_blank"
                     role="button"
                     ><i class="my-icon fab fa-twitter"></i
                  ></a>

                  <a
                     class="primary-btn btn btn-outline-light btn-floating m-1"
                     href="https://www.instagram.com/franmas99/"
                     role="button"
                     target="_blank"
                     ><i class="my-icon fab fa-instagram"></i
                  ></a>

                  <a
                     class="primary-btn btn btn-outline-light btn-floating m-1"
                     href="https://www.linkedin.com/in/jos%C3%A9-francisco-mas-lled%C3%B3-8b852b1b1/"
                     role="button"
                     target="_blank"
                     ><i class="my-icon fab fa-linkedin-in"></i
                  ></a>

                  <a
                     class="primary-btn btn btn-outline-light btn-floating m-1"
                     href="https://github.com/xexumas99"
                     role="button"
                     target="_blank"
                     ><i class="my-icon fab fa-github"></i
                  ></a>
               </section>
            </div>
            <div
               :class="isSmallScreen ? 'text-center' : 'text-end'"
               class="col-md-6 col-xs-12"
            >
               <section class="mb-4" style="font-size: 18px">
                  <p>
                     You can contact me through my social networks, email or
                     mobile phone.
                  </p>
                  <i class="primary-color fa-solid fa-envelope" />&nbsp;
                  <a class="primary-color" href="mailto:franmaslledo@gmail.com">
                     franmaslledo@gmail.com</a
                  >
                  <br />
                  <i class="primary-color fa-solid fa-phone" />&nbsp;
                  <a class="primary-color" href="tel:+34647643437">
                     +34 647 643 437</a
                  >
               </section>
            </div>
         </div>
      </div>
   </footer>
</template>

<style lang="scss" scoped>
footer {
   background: #17213c !important;

   .my-icon {
      font-size: 30px;
   }
}
</style>
