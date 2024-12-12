<script setup lang="ts">
</script>

<template>
  <div class="bg-gradient-to-b from-[#18016b] to-indigo-100 text-white min-h-screen flex flex-col items-center justify-center relative">

    <h1 class="absolute top-0 left-0 w-full text-[75px] sm:text-[200px] md:text-[300px] lg:text-[400px] text-center text-purple-500 font-bold leading-none tracking-tight opacity-10">
      PODCAST
    </h1>
    <div class="relative grid grid-cols-1 sm:grid-cols-2 md:grid-cols-12 gap-8 w-full px-4 sm:px-8 md:px-16">
      <div class="col-span-1 sm:col-span-2 md:col-span-4 flex flex-col h-full">
        <div class="flex justify-between items-center w-full">
          <span class="uppercase text-gray-400 text-sm sm:text-lg">Business</span>
          <div class="relative w-16 h-16 sm:w-20 sm:h-20 rounded-full border-4 border-dotted border-gray-400">
            <div
              class="absolute w-4 h-4 bg-gray-400 rounded-full"
              :style="{
                top: 'calc(50% - 8px)',
                left: 'calc(50% - 8px)',
                animation: 'rotate-left 4s linear infinite',
              }"
            ></div>
            <div
              class="absolute w-4 h-4 bg-gray-400 rounded-full"
              :style="{
                top: 'calc(50% - 8px)',
                left: 'calc(50% - 8px)',
                animation: 'rotate-opposite 4s linear infinite',
              }"
            ></div>
          </div>
          <span class="uppercase text-gray-400 text-sm sm:text-lg">Scaling</span>
        </div>
        <div class="flex flex-col mt-12 sm:mt-24">
          <h2 class="text-4xl sm:text-5xl md:text-7xl font-medium">Sans permission</h2>
          <p class="text-3xl sm:text-5xl md:text-7xl text-gray-300 mt-4">Le podcast qui réinvente le business.</p>
        </div>
      </div>

      <!-- Center Column (Phone Component) -->
      <div class="relative col-span-1 sm:col-span-2 md:col-span-4 flex items-center justify-center">
        <Phone />
      </div>

      <!-- Right Column -->
      <div class="col-span-1 sm:col-span-2 md:col-span-4 flex flex-col h-full mt-12 sm:mt-24">
        <div class="grid grid-cols-12 gap-4">
          <div class="col-span-12 sm:col-span-6">
            <span class="uppercase text-gray-300 text-sm sm:text-lg">Tout savoir</span>
          </div>
          <div class="col-span-12 sm:col-span-6">
            <p class="text-sm sm:text-lg text-gray-300">
              Plongez au cœur de stratégies innovantes, d'histoires inspirantes, et de conseils pratiques pour transformer vos ambitions en succès.
            </p>
          </div>
        </div>
        
        <div class="flex flex-col mt-12 sm:mt-24">
          <h2 class="text-4xl sm:text-5xl md:text-7xl font-medium">Avec Oussama, Antoine, et Yomi</h2>
          <p class="text-3xl sm:text-5xl md:text-7xl text-gray-300 mt-4">3 entrepreneurs visionnaires</p>
        </div>
      </div>
      
    </div>
  </div>
</template>

<style>
@keyframes rotate-left {
  0% {
    transform: rotate(0deg) translateX(40px); /* Rayon ajusté */
  }
  100% {
    transform: rotate(360deg) translateX(40px); /* Rayon ajusté */
  }
}

@keyframes rotate-opposite {
  0% {
    transform: rotate(180deg) translateX(40px); /* Rayon ajusté */
  }
  100% {
    transform: rotate(540deg) translateX(40px); /* Rayon ajusté */
  }
}
</style>
