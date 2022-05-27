<script lang="ts">
import { computed, defineComponent, ref } from 'vue';

export default defineComponent({
   name: 'about',
   setup() {
      const selectedOpt = ref(1);

      const isSmallScreen = computed(() => {
         return window.innerWidth < 480;
      });

      const stack = [
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
            alt: 'Angular',
            src: '/icons/angular.png',
            url: 'https://angular.io/',
         },
         {
            alt: 'GraphQl',
            src: '/icons/graphQl.png',
            url: 'https://graphql.org/',
         },
         {
            alt: 'Quasar',
            src: '/icons/quasar.png',
            url: 'https://quasar.dev/',
         },
         {
            alt: 'Git',
            src: '/icons/git.png',
            url: 'https://git-scm.com/',
         },
         {
            alt: 'MySQL',
            src: '/icons/mysql.png',
            url: 'https://mysql.com/',
         },
         {
            alt: 'Firebase',
            src: '/icons/firebase.png',
            url: 'https://firebase.google.com/',
         },
      ];

      const studies = [
         {
            center: 'Instituto Superior Europeo de Barcelona (ISEB)',
            degree:
               'Master in Business Administration and Management + Master in Big Data and Business Intelligence',
            description:
               "Currently studying a double master's degree in Business 'Administration and Managemen't and 'Big Data and Business Intelligence'.",
            from: '2021',
            to: 'now',
         },
         {
            center: 'Universidad de Alicante (UA)',
            degree: 'Degree in computer engineering',
            description:
               "Graduated with a bachelor's degree in computer engineering in the high performance group. Specialized in software engineering.",
            from: '2017',
            to: '2021',
         },
      ];

      const experience = [
         {
            company: 'Europe Language Jobs S.L.',
            position: 'Fullstack developer',
            location: 'Barcelona',
            description:
               'I am currently developing the <a class="tertiary-color" href="https://europelanguagejobs.com" target="_blank">europelanguagejobs.com</a> website with a team, while I continue working on my main project, the GoPlaces app.',
            from: '2021',
            to: 'now',
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
                  alt: 'Quasar',
                  src: '/icons/quasar.png',
                  url: 'https://quasar.dev/',
               },
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
               {
                  alt: 'Firebase',
                  src: '/icons/firebase.png',
                  url: 'https://firebase.google.com/',
               },
               {
                  alt: 'Git',
                  src: '/icons/git.png',
                  url: 'https://git-scm.com/',
               },
            ],
         },
         {
            company: 'Smartloto S.L.',
            position: 'Junior Fullstack developer',
            location: 'Alicante',
            description:
               'During my stay at smartloto S.L. I developed together with a colleague the company backoffice and a Node project that makes use of the NEM blockchain to create apostilles.',
            from: '2020',
            to: '2020',
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
               {
                  alt: 'Git',
                  src: '/icons/git.png',
                  url: 'https://git-scm.com/',
               },
            ],
         },
      ];

      function getImage(path: string) {
         return require(path);
      }

      return {
         selectedOpt,
         stack,
         studies,
         experience,
         getImage,
         isSmallScreen,
      };
   },
});
</script>

<template>
   <div id="about-section" class="section d-flex align-items-center">
      <div class="container" style="padding-top: 5em">
         <div class="row">
            <div class="col">
               <img
                  class="my-img"
                  src="http://imroz.ibthemespro.com/img/about-8.af980894.jpg"
                  alt="about_img"
               />
            </div>
            <div class="col">
               <h1>About Me</h1>
               <p style="font-size: 20px">
                  Lorem ipsum dolor sit amet consectetur adipisicing elit.
                  Impedit exercitationem beatae
               </p>
               <div
                  class="btn-group btn-group-lg"
                  role="group"
                  aria-label="Basic example"
               >
                  <button
                     @click="selectedOpt = 1"
                     type="button"
                     class="primary-btn btn btn-outline-dark btn-lg"
                     :class="selectedOpt == 1 ? 'active' : ''"
                  >
                     Stack
                  </button>
                  <button
                     @click="selectedOpt = 2"
                     type="button"
                     class="primary-btn btn btn-outline-dark btn-lg"
                     :class="selectedOpt == 2 ? 'active' : ''"
                  >
                     Studies
                  </button>
                  <button
                     @click="selectedOpt = 3"
                     type="button"
                     class="primary-btn btn btn-outline-dark btn-lg"
                     :class="selectedOpt == 3 ? 'active' : ''"
                  >
                     Experience
                  </button>
                  <button
                     @click="selectedOpt = 4"
                     type="button"
                     class="primary-btn btn btn-outline-dark btn-lg"
                     :class="selectedOpt == 4 ? 'active' : ''"
                  >
                     Interests
                  </button>
               </div>

               <div v-if="selectedOpt == 1">
                  <div class="mt-3 row gy-5">
                     <div
                        v-for="(s, index) in stack"
                        :key="index"
                        class="col-3"
                     >
                        <a :title="s.alt" :href="s.url" target="_blank">
                           <img class="my-logo" :src="s.src" :alt="s.alt" />
                        </a>
                     </div>
                  </div>
               </div>
               <div v-else-if="selectedOpt == 2">
                  <div class="mt-4">
                     <template v-for="(s, index) in studies" :key="index">
                        <span class="text-bold tertiary-color"
                           >{{ s.center }} </span
                        ><br />
                        <span class="secondary-color">{{ s.degree }} </span
                        ><br />
                        <p>{{ s.description }}</p>
                        <p class="text-end">{{ s.from }} - {{ s.to }}</p>
                     </template>
                  </div>
               </div>
               <div v-else-if="selectedOpt == 3">
                  <div class="mt-4">
                     <template v-for="(e, index) in experience" :key="index">
                        <span class="text-bold tertiary-color"
                           >{{ e.company }} - {{ e.location }} </span
                        ><br />
                        <span class="secondary-color">{{ e.position }} </span
                        ><br />
                        <p v-html="e.description" />
                        <div class="row">
                           <div class="col-10">
                              <template
                                 v-for="(s, index) in e.stack"
                                 :key="index"
                              >
                                 <a
                                    :title="s.alt"
                                    :href="s.url"
                                    target="_blank"
                                 >
                                    <img
                                       class="my-logo-sm"
                                       :src="s.src"
                                       :alt="s.alt"
                                    />
                                 </a>
                                 &nbsp;
                              </template>
                           </div>
                           <div class="col">
                              <p class="text-end">{{ e.from }} - {{ e.to }}</p>
                           </div>
                        </div>
                        <br />
                     </template>
                  </div>
               </div>
               <div v-else-if="selectedOpt == 4">
                  <div class="mt-4">
                     <div class="row">
                        <div class="col">
                           <p class="text-bold tertiary-color mb-1">
                              Software Development
                           </p>
                           <li>Front-end Development</li>
                           <li>Back-end Development</li>
                           <li>Cross-platform Mobile Development</li>
                           <p class="text-bold mt-4 tertiary-color mb-1">
                              Systems & Cybersecurity
                           </p>
                           <li>System Installation and Administration</li>
                           <li>Pentesting</li>
                           <li>Bash & Batch Scripting</li>
                        </div>
                        <div class="col">
                           <p class="text-bold tertiary-color mb-1">
                              Project Development
                           </p>
                           <li>Teamwork & Communication</li>
                           <li></li>
                           <li></li>
                           <p class="text-bold mt-4 tertiary-color mb-1">
                              Other
                           </p>
                           <li>Video Game Programming & Game Design</li>
                           <li>Blockchain & Smart Contracts</li>
                           <li></li>
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
.active {
   border: 1px solid #ff5004;
   background: #ff5004;
   color: #0b1120;
}

.my-logo {
   max-height: 5em;
   width: auto;
}

.my-logo-sm {
   max-height: 1.7em;
   width: auto;
}

.my-img {
   max-height: 65vh;
   width: auto;
   border-radius: 20px;
}

@media only screen and (max-device-width: 480px) {
   .my-img {
      height: auto;
      width: 100%;
   }
}
</style>
