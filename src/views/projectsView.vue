<template>
  <section class="mx-5">
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
</template>

<script>
export default {
  data() {
    return {
      projects: [
        {
          title: 'Artsy',
          link: 'https://artsy-lovat.vercel.app/',
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
          title: 'Unicorn Tap',
          link: 'https://unicorn-tap-landing-page.vercel.app/',
          logo: '🦄',
        },
        {
          title: 'Ecommerce Landing Page',
          link: 'https://guileless-cendol-00a6a8.netlify.app/',
          logo: '🛒',
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
.hover\:scale-105:hover {
  transform: scale(1.05);
}
.transition-transform {
  transition: transform 0.3s ease-in-out;
}
</style>
