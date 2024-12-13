<script setup lang="ts">
</script>

<template>
  <section class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-12 max-h-screen px-5 sm:px-10 md:px-20 lg:px-32 mt-10 space-x-5 sm:space-x-10">
    <div class="col-span-12 sm:col-span-6 lg:col-span-4 mt-10 sm:mt-14">
      <div>
        <h1 class="text-lg sm:text-xl font-medium">Transformez vos compétences en revenus grâce à l'infopreneuriat. <span class="text-[#29ce45]">23</span></h1>
        <div class="w-full mt-1 h-[1px] bg-black"></div>
        <p class="mt-3 sm:mt-5 text-sm sm:text-base">Antoine Blanco vous aide à transformer vos compétences en revenus grâce à des formations en ligne rentables.</p>
      </div>
      <div class="relative mt-10 sm:mt-14 h-[20rem] sm:h-[30rem]">
        <img src="@/assets/images/antoine.jpg" class="w-full rounded-3xl h-full bg-cover object-cover absolute" alt="">
        <div class="relative grid grid-cols-12 p-5 justify-between h-full">
          <div class="flex items-start gap-2 text-white col-span-12 justify-center">
            <div class="bg-black/10 border-white/50 border backdrop-blur-2xl flex gap-2 py-2 rounded-full px-5">
              <IconsBadge/>
              <h3>Coaching</h3>
            </div>
            <div class="bg-black/30 border-white/50 border backdrop-blur-2xl flex gap-2 py-2 rounded-full px-5">
              <IconsBadge/>
              <h3>Croissance</h3>
            </div>
          </div>
          <div class="z-20 absolute bottom-5 left-5">
            <ul class="flex gap-3">
              <li class="w-5 h-5 bg-white/30 rounded-full"></li>
              <li class="w-5 h-5 "></li>
            </ul>
            <ul class="flex gap-3 mt-3">
              <li class="w-5 h-5 bg-white/60 rounded-full"></li>
              <li class="w-5 h-5 bg-white/60 rounded-full"></li>
            </ul>
          </div>
          <div 
            class="bg-white/10 text-white backdrop-blur-md rounded-3xl absolute top-3/4 left-1/2 -translate-y-1/2 -translate-x-1/2 px-5 py-7 z-[9999] w-3/4 border border-white/20"
          >
            <div class="flex justify-between items-center gap-10">
              <h1 class="text-2xl sm:text-4xl font-semibold">+10k/MRR</h1>
              <IconsArrowUp/>
            </div>
            <p class="mt-3 text-white text-sm sm:text-base">Transformez vos compétences en revenus grâce à l'infopreneuriat.</p>
          </div>
        </div>
      </div>
    </div>
    <!-- Section 2 -->
    <div class="col-span-12 sm:col-span-6 lg:col-span-4 relative bg-[#18016b] rounded-3xl mt-10 sm:mt-14">
      <img src="@/assets/images/Yomi-Denzel.-1-removebg-preview.png" class=" rounded-lg   z-20" alt="">
      <h1 class="text-6xl sm:text-[10rem] font-medium absolute left-1/2 -translate-x-1/2 text-white">YOMI</h1>
      <div class="relative z-20 h-full w-full">
        <div class="absolute col-auto right-5 top-5">
          <ul class="flex gap-3">
            <li class="w-5 h-5 bg-white/50 rounded-full"></li>
            <li class="w-5 h-5 bg-white/50 rounded-full"></li>
          </ul>
          <ul class="flex gap-3 mt-3">
            <li class="w-5 h-5"></li>
            <li class="w-5 h-5 bg-white/50 rounded-full"></li>
          </ul>
        </div>
        <div 
          class="bg-white/10 w-3/4 text-white backdrop-blur-lg rounded-3xl absolute top-2/3 left-1/2 -translate-y-1/2 border border-white/20 -translate-x-1/2 p-5 z-[9999] "
        >
          <div class="flex justify-between items-center gap-10">
            <h1 class="text-2xl sm:text-4xl font-semibold">+75k/MRR</h1>
            <IconsArrowUp/>
          </div>
          <p class="mt-3 text-white text-sm sm:text-lg">
            Maîtrisez le dropshipping et développez un e-commerce à succès. <br>
            Transforme vos ambitions en boutiques en ligne à succès.
          </p>
        </div>
        <div class="relative flex items-end h-full justify-between p-5">
          <div class="col-auto left-5 bottom-5 absolute">
            <ul class="flex gap-3">
              <li class="w-5 h-5 bg-white/50 rounded-full"></li>
              <li class="w-5 h-5 "></li>
            </ul>
            <ul class="flex gap-3 mt-3">
              <li class="w-5 h-5 bg-white/50 rounded-full"></li>
              <li class="w-5 h-5 bg-white/50 rounded-full"></li>
            </ul>
          </div>
          <div class="flex gap-2 text-white">
            <div class="bg-white/10 border-white/50 border backdrop-blur-2xl flex gap-2 py-2 rounded-full px-5">
              <IconsBadge/>
              <h3>Dropshiping</h3>
            </div>
            <div class="bg-white/10 border-white/50 border backdrop-blur-2xl flex gap-2 py-2 rounded-full px-5">
              <IconsBadge/>
              <h3>E-commerce</h3>
            </div>
          </div>
        </div>
      </div>
    </div>
    <!-- Section 3 -->
    <div class="col-span-12 sm:col-span-6 lg:col-span-4 mt-10 sm:mt-14">
      <div>
        <h1 class="text-lg sm:text-xl font-medium">Des conseils sur mesure pour vos projets entrepreneuriaux.</h1>
        <div class="w-full mt-1 h-[1px] bg-black"></div>
        <p class="mt-3 sm:mt-5 text-sm sm:text-base">
          Avec "Better Call with Ouss", Oussama guide les entrepreneurs vers des décisions stratégiques. Chaque appel est une opportunité de débloquer votre potentiel.
        </p>
      </div>
      <div class="relative mt-10 sm:mt-14 h-[20rem] sm:h-[30rem]">
        <img src="@/assets/images/ouss.jpg" class="w-full rounded-3xl h-full bg-cover object-cover absolute" alt="">
        <div class="relative grid grid-cols-12 p-5 justify-between h-full">
          <div class="flex items-start gap-2 text-white col-span-12 justify-end">
            <div class="bg-white/10 border-white/50 border backdrop-blur-2xl flex gap-2 py-2 rounded-full px-5">
              <IconsBadge/>
              <h3>Entrepreneuriat</h3>
            </div>
            <div class="bg-white/10 border-white/50 border backdrop-blur-2xl flex gap-2 py-2 rounded-full px-5">
              <IconsBadge/>
              <h3>Conseils</h3>
            </div>
          </div>
          <div class="z-20 absolute bottom-5 left-5">
            <ul class="flex gap-3">
              <li class="w-5 h-5 bg-white/30 rounded-full"></li>
              <li class="w-5 h-5 "></li>
            </ul>
            <ul class="flex gap-3 mt-3">
              <li class="w-5 h-5 bg-white/60 rounded-full"></li>
              <li class="w-5 h-5 bg-white/60 rounded-full"></li>
            </ul>
          </div>
          <div 
            class="bg-white/10 text-white backdrop-blur-md rounded-3xl absolute top-3/4 left-1/2 -translate-y-1/2 -translate-x-1/2 px-5 py-7 z-[9999] w-3/4 border border-white/20"
          >
            <div class="flex justify-between items-center gap-10">
              <h1 class="text-2xl sm:text-4xl font-semibold">+500k/MRR</h1>
              <IconsArrowUp/>
            </div>
            <p class="mt-3 text-white text-sm sm:text-base">Améliorez vos projets entrepreneuriaux avec un mentor expérimenté.</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
