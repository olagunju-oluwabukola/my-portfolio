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
            date: 'August, 2024 - Present',
            description: `At Expansion Cyber Technologies I am responsible for implementing responsive landing pages, 
              developing reusable UI components, and writing type-safe client-side code. I developed and launched their landing page, among others projects
              ensuring a responsive and user-friendly design. I collaborate with cross-functional teams to deliver critical features.`,
            logo: 'https://www.expansioncybertech.com/wp-content/uploads/2024/04/logo-combo-new.png' 
          },
          {
            company: 'Microsoft Learners Student Ambassador',
            title: 'Frontend Tutor',
            date: 'August 10, 2023 - August 22, 2023',
            description: `As a Frontend tutor at MLSA skillup training, I walked the participants through the basics of fronted with HTML, CSS, and JavaScript, at the end, they were able to create a static webpage on theri own, showcasing a landing page and a contact form.`,
            logo: 'data:image/jpeg;base64,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'
          },
          
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
  