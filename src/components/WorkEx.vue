<template>
  <div class="container">
    <h2 class="font-bold text-3xl md:text-5xl mx-5 md:mx-10 my-5 md:my-10">
      Work Experience
    </h2>

    <div class="relative">
      <div class="border-l-2 border-green-500 absolute left-7 top-0 bottom-0"></div>

      <div v-for="(step, index) in steps" :key="index" class="mb-10 flex items-start relative">
        <div class="w-20 flex flex-col items-center">
          <div class="flex items-center justify-center w-14 h-14 rounded-full bg-white border-2 border-green-500 p-2 z-10">
            <img :src="step.logo" :alt="step.company + ' logo'" class="w-full h-full object-contain">
          </div>
          <div
            v-if="index < steps.length - 1"
            class="w-px h-full bg-gray-300 mt-4"
          ></div>
        </div>

        <div class="ml-8 experience-card">
          <h3 class="text-lg font-bold">{{ step.company }}</h3>
          <p class="text-sm text-green-500">{{ step.title }}</p>
          <p class="text-sm mt-1 text-gray-500">{{ step.date }}</p>
          <p class="text-sm mt-4">{{ step.description }}</p>
        </div>
      </div>
    </div>
  </div>
  <hr />
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
              ensuring a responsive and user-friendly design.`,
          logo: '/logo-combo-new.png',
        },
        {
          company: 'RedNotice',
          title: 'Frontend Developer',
          date: 'November - December, 2024',
          description: `
            I built the landing page for a cybersecurity product at RedNotice, including features such as login/signup, pricing, testimonials, and a newsletter signup form. I collaborated with the backend developer to ensure seamless integration and functionality across the site.`,
          logo: '/rednotice.svg',
        },
        {
          company: 'Project Partners Data Solution',
          title: 'Frontend Developer',
          date: 'Freelancing',
          description: `
            The project included designing and implementing features such as data visualization sections, service highlights, client testimonials, and a contact form. I worked closely with the team to ensure the website accurately reflected their brand and provided a satisfactory user experience.`,
          logo: '/ppds.jfif',
        },
        {
          company: 'InstaMediRx',
          title: 'Frontend Developer (Volunteer)',
          date: 'August, 2024 - Present',
          description: `
            As a volunteer at InstaMediRx, I contributed to the development of an application designed to connect doctors and pharmacists with their clients. The app featured booking systems, online and physical consultation options, and user-friendly interfaces for easy navigation, while providing an intuitive and reliable experience.`,
          logo: '/InstamedixLogo.png',
        },
      ],
    };
  },
};
</script>

<style scoped>
.container {
  padding: 2.5rem 1.25rem;
}

.experience-card {
  background-color: white;
  padding: 1.5rem;
  border-radius: 0.5rem;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  transition: box-shadow 0.3s ease-in-out;
}

.experience-card:hover {
  box-shadow: 0 6px 10px rgba(0, 0, 0, 0.15);
}

.relative {
  position: relative;
}

.absolute {
  position: absolute;
}
</style>
