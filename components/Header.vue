<script setup>
import { ref, onMounted } from 'vue';
import gsap from 'gsap';

const isMenuOpen = ref(false);

const toggleMenu = () => {
  isMenuOpen.value = !isMenuOpen.value;

  const menu = document.querySelector('.mobile-menu');
  const lines = document.querySelectorAll('.burger-line');

  if (isMenuOpen.value) {
    // Animate menu open
    gsap.to(menu, { x: 0, duration: 0.5, ease: 'power2.out' });

    // Animate burger to "X"
    gsap.to(lines[0], { y: 8, rotation: 45, duration: 0.3 });
    gsap.to(lines[1], { scaleX: 0, duration: 0.3 }); // ScaleX instead of opacity
    gsap.to(lines[2], { y: -8, rotation: -45, duration: 0.3 });
  } else {
    // Animate menu close
    gsap.to(menu, { x: '-100%', duration: 0.5, ease: 'power2.in' });

    // Animate burger back to initial state
    gsap.to(lines[0], { y: 0, rotation: 0, duration: 0.3 });
    gsap.to(lines[1], { scaleX: 1, duration: 0.3 }); // Reset scaleX
    gsap.to(lines[2], { y: 0, rotation: 0, duration: 0.3 });
  }
};

</script>

<template>
  <header class="bg-[#18016b] py-2 text-lg flex justify-between text-white items-center px-8 sm:px-32 relative">
    <!-- Logo -->
    <nuxt-link to="/">
      <img src="@/assets/images/channels4_profile.jpg" class="w-20 h-20 sm:w-24 sm:h-24" alt="Logo">
    </nuxt-link>

    <!-- Burger button -->
    <button 
      class="sm:hidden z-50 flex flex-col justify-center items-center w-10 h-10 relative" 
      @click="toggleMenu"
    >
      <span class="burger-line z-50 w-10 h-0.5 bg-white absolute top-2"></span>
      <span class="burger-line z-50 w-10 h-0.5 bg-white absolute top-1/2 -translate-y-1/2"></span>
      <span class="burger-line z-50 w-10 h-0.5 bg-white absolute bottom-2"></span>
    </button>

    <!-- Navigation for larger screens -->
    <nav class="hidden sm:block">
      <ul class="flex space-x-28">
        <li class="cursor-pointer nav-item">
          <nuxt-link class="relative" to="">
            <span>Home</span>
          </nuxt-link>
          <span class="border-anim"></span>
        </li>
        <li class="cursor-pointer nav-item">
          <nuxt-link class="relative" to="">
            <span>Podcast</span>
            <span class="absolute -top-3 font-bold text-sm">1.6k</span>
          </nuxt-link>
          <span class="border-anim"></span>
        </li>
        <li class="cursor-pointer nav-item">
          <nuxt-link to="" class="relative">
            <span>Articles</span>
            <span class="absolute -top-3 font-bold text-sm">200</span>
          </nuxt-link>
          <span class="border-anim"></span>
        </li>
        <li class="cursor-pointer nav-item">
          <nuxt-link to="">
            Talk to us
          </nuxt-link>
          <span class="border-anim"></span>
        </li>
      </ul>
    </nav>

    <!-- Mobile menu -->
    <nav 
      class="mobile-menu sm:hidden z-20 fixed top-0 left-0 w-full h-screen bg-[#18016b] text-white transform -translate-x-full flex flex-col items-center pt-20 space-y-8"
    >
      <ul>
        <li class="cursor-pointer nav-item">
          <nuxt-link class="relative" to="">
            <span>Home</span>
          </nuxt-link>
          <span class="border-anim"></span>
        </li>
        <li class="cursor-pointer nav-item">
          <nuxt-link class="relative" to="">
            <span>Podcast</span>
          </nuxt-link>
          <span class="border-anim"></span>
        </li>
        <li class="cursor-pointer nav-item">
          <nuxt-link to="" class="relative">
            <span>Articles</span>
          </nuxt-link>
          <span class="border-anim"></span>
        </li>
        <li class="cursor-pointer nav-item">
          <nuxt-link to="">
            Talk to us
          </nuxt-link>
          <span class="border-anim"></span>
        </li>
      </ul>
    </nav>
  </header>
</template>

<style scoped>
.nav-item {
  position: relative;
  padding-bottom: 8px;
}

.border-anim {
  position: absolute;
  bottom: 0;
  left: 0;
  width: 0%;
  height: 1px;
  background-color: white;
  transition: width 0.3s ease;
}

.nav-item:hover .border-anim {
  width: 100%;
}

.burger-line {
  transition: all 0.3s ease;
  transform-origin: center; /* Ensure proper pivot point */
  display: block; /* Ensure the span remains visible */
}

.burger-line:nth-child(2) {
  transform: scaleX(1); /* Default scale to ensure visibility */
}
</style>
