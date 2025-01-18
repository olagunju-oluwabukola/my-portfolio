<template>
  <section class="md:flex mx-5 md:mx-10 my-5 md:my-5" id="about"
  >
    <div class="grid place-item-center">
      <h1 class="font-bold text-3xl  md:text-5xl about">Frontend Software Engineer & Technical Writer</h1>
      <p class="md:text-xl text-sm mt-3">I’m Olagunju Oluwabukola Sussanah, a Software Engineer with 
     experience in building user interfaces for 
         digital web products. I prioritize excellence, simplicity 
         and speed with a goal to deliver high-quality work that 
         exceed expectations. <br />
        I enjoy studying documentation and trying out new things.</p>
    </div>
   <div class="grid place-items-center pt-5">
    <div>
      <img 
  class="md:w-[900px] rounded-full border border-yellow-500 shadow-[0_0_10px_5px_rgba(255,223,0,0.75)]" 
  src="/meee.jfif" 
  alt="Profile Picture" 
/>

     <a href="/assets/Oluwabukola Olagunju Resumê.pdf" download="Oluwabukola_Resume.pdf" class="bg-yellow-500 ml-2 rounded-xl text-white p-3 mt-3 cursor-pointer">
    Download Resume
    </a>
      <div class="flex mt-3">
        <img
          class="h-5 w-5"
          src="http://ts4.mm.bing.net/th?id=OIP.EfG8OZzwC_nZibphM8vQPAHaHa&pid=15.1"
          alt=""
        />
        <a
          href="mailito:olagunjuoluwabukola2018@gmail.com"
          target="_blank"
          rel="noopener noreferrer"
          >olagunjuoluwabukola2018@gmail.com</a
        >
      </div>
    </div>
 
   </div>
  </section>

  <div class="flex gap-4 mx-5 md:mx-10 my-10 md:my-5 underline">
    <a href="https://www.linkedin.com/in/oluwabukola-olagunju-434512229" class="flex"><img class="w-4 h-5" src="/public/LinkedIn.svg" alt=""> LinkedIn </a>
    <a href="https://www.twitter.com/ofeyishayomi3" class="flex"><img class="w-4 h-5" src="/public/Twitter X.svg" alt=""> Twitter</a>
    <a href="https://Github.com/olagunju-oluwabukola" class="flex"><img class="w-6 h-5" src="https://logos-world.net/wp-content/uploads/2020/11/GitHub-Symbol.png" alt=""> Github</a>
    <a href="https://medium.com/@olagunjuoluwabukola2018/" class="flex"><img class="w-5 h-5" src="data:image/jpeg;base64,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" alt=""> Medium </a>
  </div>

  <div class="">
    <p class="font-bold text-2xl md:text-5xl mb-6 mx-10">Expertise</p>
    <div class="mx-10">
      I've spent few years working on my skills. In no particular order, here are a few of them.
    </div>
  </div>
  <div class="flex gap-3 mt-3 md:m-10 justify-center md:justify-start">
    <li>Vue</li>
    <li>React</li>
    <li>Firebase</li>
    <li>Tailwind</li>
    <li>Bootstrap</li>
    <li>Vuetify</li>
   
  </div>

  <work-ex/>
  <section class="mx-5" id="project"
  >
    <div class="font-bold text-3xl md:text-5xl mx-5 md:mx-10 my-5 md:my-10">
      Welcome to my Projects Showcase
    </div>
    <div class="mx-5 md:w-1/2 md:mx-10">
      I've worked on tons of little projects over the years, but these
      are the ones that I'm most proud of. Some of them are open-source, 
      so if you see something that piques your interest, 
      check them out and explore the possibilities!
    </div>

    <div class="grid md:grid-cols-2 gap-10 md:mx-10 mt-5 md:mt-8">
      <a
        v-for="project in projects"
        :key="project.title"
        :href="project.link"
        target="_blank"
        rel="noopener noreferrer"
        class="border rounded-lg shadow-lg p-4 flex justify-between items-center px-5 md:px-10 transition-transform transform hover:scale-105"
      >

        <div class="h-12 w-12 flex items-center justify-center bg-gray-200 rounded-full">
          
          <template v-if="isImage(project.logo)">
            <img :src="project.logo" :alt="project.title + ' logo'" class="w-full h-full object-contain rounded-full" />
          </template>
          <template v-else>
            <span class="text-lg font-bold">{{ project.logo }}</span>
          </template>
        </div>
        
        <div class="font-semibold">{{ project.title }}</div>
      </a>
    </div>
  </section>

  <div class="mt-10" id="blog-section"> 
    <div class="font-bold text-3xl md:text-5xl text-center mt-2 md:mt-5">
    
    Visit my profile on  <a href=" https://medium.com/@olagunjuoluwabukola2018/" class="underline">Medium</a> to read some of my articles😊.
    
   </div>
   <a href=" https://medium.com/@olagunjuoluwabukola2018/" target="_blank" rel="noopener noreferrer">
    <img class="mx-auto mt-3 h-72" src="data:image/jpeg;base64,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" alt=""> 
   </a>
  </div>  
</template>

<script>

import WorkEx from '@/components/WorkEx.vue';
export default {
  components: 
  {
    WorkEx
  },
  data() {
    return {
      boxes: [1, 2, 3], 
      projects: [
        {
          title: 'Artsy',
          link: 'https://artsy-rhq2.vercel.app/',
          logo: '🎨',
        },
        {
          title: 'Ppds',
          link: 'https://ppds-4ifk.vercel.app/',
          logo: '/ppds.jfif',
        },
        {
          title: 'Red Notice',
          link: 'https://red-notice-wdyt.vercel.app/',
          logo: '/rednotice.svg',
        },
        {
          title: 'Gericht',
          link: 'https://gericht-resturant-app.netlify.app/',
          logo: '🍽️',
        },
        {
          title: 'She Code Africa Website Replication',
          link: 'https://sca-clone.vercel.app/',
          logo: '/sca.svg',
        },
        
        {
          title: 'Expansion Cybertech Sales Landing Page',
          link: 'https://ect-sales-page.vercel.app/',
          logo: '/logo-combo-new.png',
        },
      ],
    };
  },

  methods: {
    isImage(logo) {

      return logo.startsWith('/') || logo.startsWith('http');
    },
  },
};
</script>

<style>
@keyframes flow {
  0% {
    transform: translateY(0%);
  }
  50% {
    transform: translateY(50%);
  }
  100% {
    transform: translateY(0%);
  }
}

.animate-flow {
  animation: flow 2s infinite;
}

li {
  list-style: none;
  background: green;
  color: #fff;
  padding: 5px;
  border-radius: 10px;
}

.hover\:scale-105:hover {
  transform: scale(1.05);
}
.transition-transform {
  transition: transform 0.3s ease-in-out;
}
</style>
