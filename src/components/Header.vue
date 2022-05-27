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
         <h1 style="font-size: 70px !important; color: #ff5004">
            Fran Mas Lledó
         </h1>
         <h2 style="font-size: 50px !important">Fullstack developer</h2>
         <button
            type="button"
            class="mt-3 btn btn-outline-dark btn-lg"
            style="
               color: #ff5004;
               border: 1px solid #ff5004;
               border-radius: 20px;
            "
         >
            Download CV
         </button>
      </div>
   </div>
</template>

<style lang="scss" scoped>
#header-section {
   min-height: 100vh;
}
</style>
