<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
   name: 'header',
   setup() {
      return {};
   },
});
</script>

<template>
   <div id="header-section" class="section d-flex align-items-center">
      <div class="container">
         <h1 class="primary-color" style="font-size: 70px !important">
            Fran Mas Lledó
         </h1>
         <h2 style="font-size: 50px !important">Fullstack developer</h2>

         <a
            href="https://drive.google.com/file/d/1WfOEXNGdyHr3LP-Bkqb-xHzl-NFg2a2o/view?usp=sharing"
            target="_blank"
         >
            <button
               type="button"
               class="mt-3 btn btn-outline-dark btn-lg tertiary-btn"
            >
               Download CV
            </button>
         </a>
      </div>
   </div>
</template>

<style lang="scss" scoped>
#header-section {
   min-height: 100vh;
}
</style>
