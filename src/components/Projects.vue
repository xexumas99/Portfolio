<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
   name: 'projects',
   setup() {
      const projects = [
         {
            title: 'Undecimo Backoffice',
            company: 'Smartloto S.L.',
            description:
               'Development of an administration page to control the apostilled lottery tickets on the NEM blockchain, made in laravel framework.',
            stack: [
               {
                  alt: 'Laravel',
                  src: '/icons/laravel.png',
                  url: 'https://laravel.com/',
               },
               {
                  alt: 'NodeJS',
                  src: '/icons/node.png',
                  url: 'https://nodejs.org/',
               },
               {
                  alt: 'MySQL',
                  src: '/icons/mysql.png',
                  url: 'https://mysql.com/',
               },
            ],
            repository: null,
            url: null,
            doc: null,
         },
         {
            title: 'GoPlaces',
            company: 'Europe Language Jobs',
            description:
               'A light but powerful mobile application to find the best places to work in Europe. Developed in Flutter for Android and IOS.',
            repository: null,
            url: null,
            doc: null,
            stack: [
               {
                  alt: 'Flutter',
                  src: '/icons/flutter.svg',
                  url: 'https://flutter.dev/',
               },
               {
                  alt: 'NodeJS',
                  src: '/icons/node.png',
                  url: 'https://nodejs.org/',
               },
               {
                  alt: 'MySQL',
                  src: '/icons/mysql.png',
                  url: 'https://mysql.com/',
               },
            ],
         },
         {
            title: 'Colors',
            company: 'Myself',
            description:
               'A small project made in Laravel and Vue that gets the most dominant color of an image, it also tries to guess its name.',
            repository: 'https://github.com/xexumas99/colores',
            url: null,
            doc: null,
            stack: [
               {
                  alt: 'Laravel',
                  src: '/icons/laravel.png',
                  url: 'https://laravel.com/',
               },
            ],
         },
         {
            title: 'AcademiaOnline ',
            company: 'Myself',
            description:
               'An initiation project for a GraphQL API made in JS. It emulates an academyand you can use it by http requests or an UI.',
            repository: 'https://github.com/xexumas99/AcademiaOnline',
            url: null,
            doc: null,
            stack: [
               {
                  alt: 'GraphQl',
                  src: '/icons/graphQl.png',
                  url: 'https://graphql.org/',
               },
               {
                  alt: 'NodeJS',
                  src: '/icons/node.png',
                  url: 'https://nodejs.org/',
               },
            ],
         },

         {
            title: 'Fran Chess Game ',
            company: 'Myself',
            description:
               "A simple chess game made in JS. It also lets you save/load your games and check the opening. It's playable but some rules are missing.",
            repository: null,
            url: 'https://fran-chess-game.netlify.app/',
            doc: null,
            stack: [
               {
                  alt: 'Angular',
                  src: '/icons/angular.png',
                  url: 'https://angular.io/',
               },
            ],
         },
         {
            title: 'Teacher At Home',
            company: 'Myself',
            description:
               "My final degree project in college, it's a whole environment, with a mobile app, backoffice page, public API and a website.",
            repository: null,
            url: null,
            doc: 'https://drive.google.com/file/d/1Tmg_ReL3FESgQXHian3PD3jmQMjYl8A0/view?usp=sharing',
            stack: [
               {
                  alt: 'Flutter',
                  src: '/icons/flutter.svg',
                  url: 'https://flutter.dev/',
               },
               {
                  alt: 'Vue',
                  src: '/icons/vue.png',
                  url: 'https://vuejs.org/',
               },
               {
                  alt: 'NodeJS',
                  src: '/icons/node.png',
                  url: 'https://nodejs.org/',
               },
               {
                  alt: 'React',
                  src: '/icons/react.png',
                  url: 'https://reactjs.org/',
               },
               {
                  alt: 'Svelte',
                  src: '/icons/svelte.png',
                  url: 'https://svelte.dev/',
               },
               {
                  alt: 'Firebase',
                  src: '/icons/firebase.png',
                  url: 'https://firebase.google.com/',
               },
            ],
         },
      ];

      return { projects };
   },
});
</script>

<template>
   <div id="projects-section" class="section">
      <div class="container">
         <h1 class="text-center" style="padding-top: 2em">My Projects</h1>

         <div class="row pt-4">
            <div
               v-for="(project, index) in projects"
               :key="index"
               class="col-md-4 col-xs-12"
            >
               <div
                  class="card mt-4"
                  style="
                     background: #17213c;
                     border: 1px solid #fa7840;
                     border-radius: 20px;
                     box-shadow: 2px 2px 5px 2px #fa7840;
                  "
               >
                  <div class="card-body">
                     <h5 class="card-title" style="color: #ff5004">
                        {{ project.title }}
                     </h5>
                     <h6 class="card-subtitle mb-2 text-muted">
                        For: {{ project.company }}
                     </h6>
                     <p class="card-text">
                        {{ project.description }}
                     </p>
                     <div class="row">
                        <div
                           v-if="project.repository != null"
                           class="col-md-4 col-xs-12"
                        >
                           <a
                              :href="project.repository"
                              target="_blank"
                              class="card-link"
                              style="color: #ffcd9b"
                              >Repository</a
                           >
                        </div>
                        <div
                           v-if="project.url != null"
                           class="col-md-2 col-xs-12"
                        >
                           <a
                              :href="project.url"
                              target="_blank"
                              class="card-link"
                              style="color: #ffcd9b"
                              >View</a
                           >
                        </div>
                        <div
                           v-if="project.doc != null"
                           class="col-md-2 col-xs-12"
                        >
                           <a
                              :href="project.doc"
                              target="_blank"
                              class="card-link"
                              style="color: #ffcd9b"
                              >Paper</a
                           >
                        </div>
                        <div class="col text-end">
                           <template
                              v-for="(s, index) in project.stack"
                              :key="index"
                           >
                              <a :href="s.url" target="_blank">
                                 <img
                                    :title="s.alt"
                                    class="my-logo"
                                    :src="s.src"
                                    :alt="s.alt"
                                 />
                              </a>
                              &nbsp;
                           </template>
                        </div>
                     </div>
                  </div>
               </div>
            </div>
         </div>
      </div>
   </div>
</template>

<style lang="scss" scoped>
.my-logo {
   max-height: 1.7em;
   width: auto;
}
</style>
