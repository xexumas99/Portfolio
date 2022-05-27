<script lang="ts">
import { defineComponent } from 'vue';
import About from './components/About.vue';
import Bottombar from './components/Bottombar.vue';
import Header from './components/Header.vue';
import Navbar from './components/Navbar.vue';
import Projects from './components/Projects.vue';

export default defineComponent({
   components: { Header, About, Projects, Navbar, Bottombar },
   name: 'App',
   setup() {
      return {};
   },
});
</script>

<template>
   <Navbar />

   <Header />

   <About />

   <Projects class="pb-5" />
   <Bottombar />
</template>

<style scoped lang="scss">
@import url('./assets/main.scss');
</style>
