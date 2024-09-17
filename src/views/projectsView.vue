<template>
  <section class="mx-5">
    <div class="font-bold text-3xl md:text-5xl mx-5 md:mx-10 my-5 md:my-10">
    Welcome to my Projects Showcase
  </div>
  <div class="mx-5 md:w-1/2 md:mx-10 ">
    I've worked on tons of little projects over the years but these
     are the ones that I'm most proud of. some of them are open-source, 
     so if you see something that piques your interest, 
    check out the code and contribute if you have ideas for how it can be improved.</div>

    <div class="grid md:grid-cols-2 gap-10 md: mx-10 mt-5 md:mt-8">
      <div v-for="project in projects" :key="project">
        <p class="font-bold text-xl md:text-2xl mb-3">{{ project.title }}</p>
        <a :href=project.link><img :src= project.img class="md:h-72"></a>
        <p class="mt-3">{{ project.description }}</p>
        
<img src="" alt="">
      </div>
    </div>
  </section>
  
</template>

<script>
import img1 from '/gericht.png'
import img2 from '/cweinshop.png'
import img3 from '/ect.png'
import img4 from '/unicorn.png'
export default {
data(){
  return {
    projects: [
      {
        title: 'Gericht',
        description: 'Gericht is a  multipage web app  that demonstrates the usage of Vue.js, firebase, vue router, axios and Tailwind CSS in creating a web application for resturant usage. I has features like blog post, Newsletter subscription and reservation.',
        link: 'https://gericht-resturant-app.netlify.app/',
        img: img1
      },
      {
        title: 'Unicorn Tap',
        description: 'Unicorn tap is simple project that features the usage of Vue.js,  Tailwind CSS in creating a web application for a cryptocurency landing page.',
        link: 'https://unicorn-tap-landing-page.vercel.app/',
        img: img4
      },
      {
        title: 'Ecommerce landing Page',
        description: 'CwetheinShop is an onine store landing page that allows you to buy shoes,  also has a mockup payment option and also a product carousel to showcase the available products.',
        link: 'https://guileless-cendol-00a6a8.netlify.app/',
        img: img2
      },
      {
        title: 'Expansion Cybertech Sales Landing page',
        description: 'Expansion Cybertech Sales Landing page is a multipage web application showing the details of services the company provides interms of website services. It is a fully responsive app made with vuejus and tailwind css.',
        link: 'https://ect-sales-page.vercel.app/',
        img: img3
      },
      
    
    ]
  }
}
}
</script>

<style>

</style>