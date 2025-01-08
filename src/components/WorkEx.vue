<template>
    <div class="container ">
      <h2 class="font-bold text-3xl md:text-5xl mx-5 md:mx-10 my-5 md:my-10">Work Experience</h2>
  
    
      <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
        
        <div v-for="(step, index) in steps" :key="index" class="relative">
          <div class="flex items-start mb-10 relative">
          
            <div class="flex flex-col items-center mr-8 relative">
          
              <div class="flex items-center justify-center w-14 h-14 rounded-full bg-white border-2 border-green-500 p-2 z-10">
                <img :src="step.logo" :alt="step.company + ' logo'" class="w-full h-full object-contain">
              </div>
  
             
              <div 
                v-if="index < steps.length - 1" 
                class="absolute top-full left-1/2 w-px h-full bg-gray-300"
              ></div>
            </div>
  
            <div class="experience-card">
              <div class="flex items-center">
                <div>
                  <h3 class="text-lg font-bold">{{ step.company }}</h3>
                  <p class="text-sm">{{ step.title }}</p>
                </div>
              </div>
              <p class="text-sm mt-2">{{ step.date }}</p>
              <p class="text-sm mt-4">{{ step.description }}</p>
            </div>
          </div>
        </div>
      </div>
    </div>
    <hr>
  </template>
  
  <script>
  export default {
    data() {
      return {
        steps: [
          {
            company: 'Expansion Cyber Technologies',
            title: 'Frontend Developer Intern',
            date: 'August, 2024 - October, 2024',
            description: `At ECT I was responsible for implementing responsive landing pages, 
              developing reusable UI components, and writing type-safe client-side code. I developed the landing page, among other projects
              ensuring a responsive and user-friendly design. `,
            logo: 'https://www.expansioncybertech.com/wp-content/uploads/2024/04/logo-combo-new.png' 
          },
          {
            company: 'RedNotice',
            title: 'Frontend Developer',
            date: 'November - December, 2024',
            description: `
            I built the landing page for a cybersecurity product at RedNotice, including features such as login/signup, pricing, testimonials, and a newsletter signup form. I collaborated with the backend developer to ensure seamless integration and functionality across the site.`,
            logo: "/rednotice.svg"
          },

          {
  company: "Project Partners Data Solution",
  title: "Frontend Developer",
  date: "Freelancing",
  description: `
 The project included designing and implementing features such as data visualization sections, service highlights, client testimonials, and a contact form. I worked closely with the team to ensure the website accurately reflected their brand and provided a satisfactory user experience.`,
  logo: "/ppds.jfif"
},
{
  company: "InstaMediRx",
  title: "Frontend Developer (Volunteer)",
  date: "August, 2024 - Present",
  description: `
As a volunteer at InstaMediRx, I contributed to the development of an application designed to connect doctors and pharmacists with their clients. The app featured booking systems, online and physical consultation options, and user-friendly interfaces for easy navigation, while providing an intuitive and reliable experience.`,
  logo: "/InstamedixLogo.png"
}


          
        ]
      }
    }
  }
  </script>
  
  <style scoped>
  .experience-card {
    @apply bg-white p-6 rounded-lg shadow-md hover:shadow-lg transition-shadow duration-300;
  }
  
  .container {
    @apply px-5 py-10;
  }
  
  .relative {
    position: relative;
  }
  
  .absolute {
    position: absolute;
   
    left: 50%;
    transform: translateX(-50%);
  }
  </style>
  