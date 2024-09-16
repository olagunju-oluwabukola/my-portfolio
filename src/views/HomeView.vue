<template>
  <section class="md:flex mx-5 md:mx-10 my-5 md:my-5">
    <div>
      <h1 class="font-bold text-3xl md:text-5xl">Frontend Software Engineer & Technical Writer</h1>
      <p class="md:text-xl text-sm mt-3">I’m Olagunju Oluwabukola Sussanah, a Software Engineer with 
     experience in building user interfaces for 
         digital web products. I prioritize excellence, simplicity 
         and speed with a goal to deliver high-quality work that 
         exceed expectations.</p>
    </div>
   <div class="flex">
    <div
      v-for="(box, index) in boxes"
      :key="index"
      class="relative w-20 h-20 md:w-36 md:h-48 mx-4 my-5 md:"
    >
      <div
        :class="[
          'absolute w-full h-full animate-flow',
          index === 0 ? 'bg-cyan-400' : index === 1 ? 'bg-green-400' : 'bg-yellow-400'
        ]"
        :style="{
          clipPath: 'polygon(50% 0%, 100% 25%, 100% 75%, 50% 100%, 0% 75%, 0% 25%)',
          animationDelay: `${index * 0.5}s` 
        }"
      >
        
      </div>
    </div>
 
   </div>
  </section>

  <div class="flex gap-4 mx-5 md:mx-10 my-10 md:my-5 underline">
    <a href="#" class="flex"><img src="/public/LinkedIn.svg" alt=""> LinkedIn </a>
    <a href="#" class="flex"><img src="/public/Twitter X.svg" alt=""> Twitter</a>
    <a href="#" class="flex"><img src="/public/LinkedIn.svg" alt=""> Github</a>
    <a href="#" class="flex"><img src="/public/LinkedIn.svg" alt=""> Medium </a>
  </div>

  <contibution-graph/>
  <work-ex/>
</template>

<script>
import ContibutionGraph from '@/components/ContibutionGraph.vue';
import WorkEx from '@/components/WorkEx.vue';
export default {
  components: 
  {ContibutionGraph,
    WorkEx
  },
  data() {
    return {
      boxes: [1, 2, 3], 
    };
  }
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
</style>
