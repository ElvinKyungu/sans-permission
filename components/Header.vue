<script setup>
import { ref } from 'vue'
import gsap from 'gsap'

const isMenuOpen = ref(false)

const toggleMenu = () => {
  isMenuOpen.value = !isMenuOpen.value
  const menu = document.querySelector('.mobile-menu')

  if (isMenuOpen.value) {
    gsap.to(menu, { x: 0, duration: 0.5, ease: "power2.out" })
  } else {
    gsap.to(menu, { x: "-100%", duration: 0.5, ease: "power2.in" })
  }
}
</script>

<template>
  <header class="bg-[#18016b] py-4 flex justify-between items-center px-8 sm:px-32 text-white relative">
    <!-- Logo -->
    <nuxt-link to="/" class="flex-shrink-0">
      <img src="@/assets/images/channels4_profile.jpg" class="w-16 sm:w-24" alt="Logo">
    </nuxt-link>

    <!-- Burger button -->
    <button 
      class="sm:hidden z-50 flex flex-col justify-center items-center space-y-1 w-10 h-10 border rounded-md border-white" 
      @click="toggleMenu"
    >
      <span class="w-6 h-0.5 bg-white"></span>
      <span class="w-6 h-0.5 bg-white"></span>
      <span class="w-6 h-0.5 bg-white"></span>
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
      class="mobile-menu sm:hidden fixed top-0 left-0 w-full h-screen bg-[#18016b] text-white transform -translate-x-full z-40 flex flex-col items-center pt-20 space-y-8"
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
</style>
