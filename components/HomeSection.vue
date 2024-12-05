<script setup lang="ts">
</script>

<template>
  <div class="bg-gradient-to-b from-[#18016b] to-indigo-100 text-white h-screen flex flex-col items-center justify-center relative">

    <h1 class="absolute top-0 left-0 w-full text-[400px] text-center text-purple-500 font-bold leading-none tracking-tight opacity-10">
      PODCAST
    </h1>
    <div class="relative grid grid-cols-12 justify-between items-start w-full px-16">
      <div class="col-span-4 justify-between h-full">
        <div class="flex justify-between items-center w-full">
          <span class="uppercase text-gray-400 text-lg">Material</span>
          <div class="relative w-20 h-20 rounded-full border-4 border-dotted border-gray-400">
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
          <span class="uppercase text-gray-400 text-lg">Material</span>
        </div>
        <div class="flex flex-col mt-36">
          <h2 class="text-7xl font-medium">Enhanced</h2>
          <p class="text-7xl text-gray-300 mt-4">Audio Quality</p>
        </div>
      </div>
      <div class="relative col-span-4 flex items-center justify-center">
        <Phone/>
      </div>

      <div class="col-span-4 justify-between h-full mt-10">
        <div class=" grid-cols-12 justify-between grid">
          <div class=" col-span-6">
            <span class="uppercase text-gray-400 text-lg">Product</span>
          </div>
          <div class=" col-span-6">
            <p class="text-gray-400 text-lg">
              Lorem ipsum dolor sit amet, consectetur adipiscing elit. Suspendisse varius.
              Lorem ipsum dolor sit amet, consectetur adipiscing elit. Suspendisse varius.
            </p>
          </div>
          
        </div>
        <div class="flex flex-col mt-36">
          <h2 class="text-7xl font-medium ">Diverse</h2>
          <p class="text-7xl text-gray-300 mt-4">Music Collection</p>
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
