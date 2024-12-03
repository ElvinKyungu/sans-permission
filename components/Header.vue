<script setup>
import { onMounted } from 'vue'
import gsap from 'gsap'

onMounted(() => {
  const navItems = document.querySelectorAll('.nav-item')

  navItems.forEach(item => {
    item.addEventListener('mouseenter', () => {
      gsap.to(item.querySelector('.border-anim'), {
        duration: 0.3,
      });
    })

    item.addEventListener('mouseleave', () => {
      gsap.to(item.querySelector('.border-anim'), {
        duration: 0.3,
      });
    })
  })
})
</script>

<template>
  <header class="bg-[#18016b] py-1 text-lg flex justify-between text-white items-center px-32">
    <nuxt-link to="/">
      <img src="@/assets/images/channels4_profile.jpg" class="w-24 h-24" alt="">
    </nuxt-link>
    <nav>
      <ul class="flex space-x-28">
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
    <nav>
      <ul class="flex space-x-6">
        <li class="cursor-pointer nav-item">
          <nuxt-link to="">
            <IconsYoutube class="text-white w-7 h-7"/>
          </nuxt-link>
          <span class="border-anim"></span>
        </li>
        <li class="cursor-pointer nav-item">
          <nuxt-link to="">
            <IconsSpotify class="text-white w-7 h-7"/>
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
