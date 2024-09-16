
<template>
  <nav class="bg-black text-white px-6 py-4 flex justify-between items-center">
    <div class="flex justify-center">
      <router-link to="/" class="hover:text-gray-400">
        <h1 class="text-3xl font-serif text-yellow font-bold">OOS</h1>
      </router-link>
    </div>

    <div class="hidden lg:flex space-x-6 mr-12">
      <router-link to="/" class="hover:text-gray-400 hover:border-b-2 border-yellow-500 pb-1">Home</router-link>
      <router-link to="/about" class="hover:text-gray-400 hover:border-b-2 border-yellow-500 pb-1">About</router-link>
      <router-link to="/blog" class="hover:text-gray-400 hover:border-b-2 border-yellow-500 pb-1">Blog</router-link>
      <router-link to="/project" class="hover:text-gray-400 hover:border-b-2 border-yellow-500 pb-1">Project</router-link>
    </div>

    <!-- Mobile Menu Button -->
    <button @click="toggleMenu" class="lg:hidden">
      <svg class="w-6 h-6 text-white" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16"></path>
      </svg>
    </button>

    <!-- Mobile Menu -->
    <transition name="fade" @before-enter="beforeEnter" @enter="enter" @leave="leave">
      <div v-if="menuOpen" class="lg:hidden absolute top-14 left-0 w-full bg-black flex flex-col space-y-4 px-6 py-4">
        <router-link to="/" class="hover:text-gray-400 hover:border-b-2 border-yellow-500 pb-1">Home</router-link>
        <router-link to="/about" class="hover:text-gray-400 hover:border-b-2 border-yellow-500 pb-1">About</router-link>
        <router-link to="/blog" class="hover:text-gray-400 hover:border-b-2 border-yellow-500 pb-1">Blog</router-link>
        <router-link to="/project" class="hover:text-gray-400 hover:border-b-2 border-yellow-500 pb-1">Project</router-link>
      </div>
    </transition>
  </nav>

  <div>
    <router-view/>
  </div>

  <footer>
    <footer-comp/>
  </footer>
</template>

<script>
import FooterComp from './components/FooterComp.vue';
export default {
  components: { FooterComp },
  data() {
    return {
      menuOpen: false,
    };
  },
  methods: {
    toggleMenu() {
      this.menuOpen = !this.menuOpen;
    },
    beforeEnter(el) {
      el.style.opacity = 0;
    },
    enter(el, done) {
      el.offsetHeight; // trigger reflow
      el.style.transition = 'opacity 0.5s';
      el.style.opacity = 1;
      done();
    },
    leave(el, done) {
      el.style.transition = 'opacity 0.5s';
      el.style.opacity = 0;
      done();
    }
  },
};
</script>

<style scoped>
.fade-enter-active, .fade-leave-active {
  transition: opacity 0.5s;
}
.fade-enter, .fade-leave-to {
  opacity: 0;
}
</style>
