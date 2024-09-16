<template>
    <div class="container mx-auto">
      <h2 class="font-bold text-3xl md:text-5xl mx-5 md:mx-10 my-5 md:my-10">Work Experience</h2>
  
      <!-- Grid Layout for the Stepper Content -->
      <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
        <!-- Step Items with Content -->
        <div v-for="(step, index) in steps" :key="index" class="relative">
          <div class="flex items-start mb-10 relative">
            <!-- Step Logo and Connector Line -->
            <div class="flex flex-col items-center mr-8 relative">
              <!-- Company Logo Circle -->
              <div class="flex items-center justify-center w-14 h-14 rounded-full bg-white border-2 border-blue-500 p-2 z-10">
                <img :src="step.logo" :alt="step.company + ' logo'" class="w-full h-full object-contain">
              </div>
  
              <!-- Connector Line (extending from the bottom of the logo) -->
              <div 
                v-if="index < steps.length - 1" 
                class="absolute top-full left-1/2 w-px h-full bg-gray-300"
              ></div>
            </div>
  
            <!-- Step Content -->
            <div class="experience-card">
              <div class="flex items-center">
                <img :src="step.logo" :alt="step.company" class="w-10 h-10 mr-4">
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
            company: 'Flincap',
            title: 'Frontend Software Engineer',
            date: 'MAY 27, 2024 - PRESENT',
            description: `At Flincap I am responsible for implementing responsive dashboard and landing pages, 
              developing reusable UI components, and writing type-safe client-side code. I collaborate with cross-functional teams to deliver critical features.`,
            logo: 'flincap-logo.png' // Replace with actual image paths
          },
          {
            company: 'Overhol',
            title: 'Frontend Software Engineer',
            date: 'NOV 13, 2023 - DEC 29, 2023',
            description: `As a Frontend Software Engineer at Overhol, I developed and launched their landing page, 
              ensuring a responsive and user-friendly design.`,
            logo: 'overhol-logo.png'
          },
          {
            company: 'Vigoe Consulting',
            title: 'Frontend Engineer',
            date: 'JAN 2, 2023 - MAR 31, 2023',
            description: `I worked as a Frontend Engineer, focusing on developing responsive web applications, improving UI components, and ensuring high performance.`,
            logo: 'vigoe-logo.png'
          },
          {
            company: 'Chain Consults',
            title: 'Frontend Developer Intern',
            date: 'JUN 1, 2022 - DEC 1, 2022',
            description: `I contributed as a Frontend Developer Intern, assisting with the development of web features and ensuring compatibility across various browsers and devices.`,
            logo: 'chain-logo.png'
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
    /* Adjust this value for positioning the line correctly between logos */
    left: 50%;
    transform: translateX(-50%);
  }
  </style>
  