<script lang="ts">
import { computed, defineComponent } from 'vue';
import About from './components/About.vue';
import Bottombar from './components/Bottombar.vue';
import Header from './components/Header.vue';
import Navbar from './components/Navbar.vue';
import Projects from './components/Projects.vue';

export default defineComponent({
   components: { Header, About, Projects, Navbar, Bottombar },
   name: 'App',
   setup() {
      const isSmallScreen = computed(() => {
         return window.innerWidth < 480;
      });
      return { isSmallScreen };
   },
});
</script>

<template>
   <Navbar :isSmallScreen="isSmallScreen" />

   <Header :isSmallScreen="isSmallScreen" />

   <About :isSmallScreen="isSmallScreen" />

   <Projects :isSmallScreen="isSmallScreen" class="pb-5" />
   <Bottombar :isSmallScreen="isSmallScreen" />
</template>

<style scoped lang="scss">
@import url('./assets/main.scss');
</style>
