<script setup lang="ts">
import videoIntro from '@/assets/videos/intro.mp4'
const isMuted = ref(true);
const videoRef = ref<HTMLVideoElement | null>(null);

const toggleMute = () => {
  isMuted.value = !isMuted.value;
  if (videoRef.value) {
    videoRef.value.muted = isMuted.value;
  }
};
</script>
<template>
  <main>
    <Header/>
    <HomeSection/>

    <section class="flex flex-col sm:flex-row items-center sm:items-start justify-between px-8 sm:px-32 py-16">
      <!-- Image -->
      <div class="flex-shrink-0 rounded-lg overflow-hidden shadow-lg w-full sm:w-1/2 mb-8 sm:mb-0">
        <img 
          src="@/assets/images/640x340_sc_ouss.jpg" 
          alt="Podcast Image" 
          class="w-full h-full object-cover"
        />
      </div>

      <!-- Content -->
      <div class="flex-1 sm:ml-12">
        <h2 class="text-4xl font-bold mb-4">Unlock Your Potential</h2>
        <p class="text-lg mb-8">With Our Self-Improvement Podcast</p>

        <!-- Episode -->
        <div class="flex items-center mb-8">
          <img 
            src="@/assets/images/antoine.jpg"
            alt="Episode Image" 
            class="w-32 h-32 rounded-lg mr-4"
          />
          <div>
            <p class="text-sm">Eps. 205 - Mastering Mindfulness:</p>
            <p class="text-sm font-bold">Finding Peace in the Present with Antoine Blanco</p>
            <button class="mt-2 text-sm text-blue-500">Play this episode</button>
          </div>
        </div>

        <!-- Stats -->
        <div class="grid grid-cols-2 gap-4">
          <div class="p-4 rounded-lg bg-gray-100 text-center">
            <p class="text-xl font-bold">340k+</p>
            <p class="text-sm">Listeners</p>
          </div>
          <div class="p-4 rounded-lg bg-green-100 text-center">
            <p class="text-xl font-bold">500k+</p>
            <p class="text-sm">Streams</p>
          </div>
        </div>

        <!-- Platforms -->
        <div class="flex space-x-4 mt-8">
          <button class="w-10 h-10 flex items-center justify-center bg-red-500 text-white rounded-full">
            Y
          </button>
          <button class="w-10 h-10 flex items-center justify-center bg-green-500 text-white rounded-full">
            S
          </button>
        </div>
      </div>
    </section>
    <!-- Real Estate Section -->
    <section class="bg-gradient-to-l from-yellow-50 to-green-50 py-16 w-full">
      <div class="grid grid-cols-1 lg:grid-cols-12 gap-8 px-4 sm:px-8 lg:px-32 w-full relative">
        <!-- Image -->
        <div class="lg:col-span-9 w-full rounded-lg overflow-hidden shadow-lg">
          <img 
            src="@/assets/images/banner.png" 
            alt="Property Image" 
            class="w-full h-64 sm:h-96 lg:h-full object-cover"
          />
        </div>
    
        <!-- Content -->
        <div class="lg:col-span-3 bg-white rounded-lg shadow-lg p-6 flex flex-col items-center">
          <!-- Property Details -->
          <div class="text-sm mb-4 w-full flex justify-between">
            <div class="flex flex-col items-center">
              <span class="text-2xl font-bold">4</span>
              <span class="text-gray-600">Beds</span>
            </div> 
            <div class="flex flex-col items-center">
              <span class="text-2xl font-bold">3</span>
              <span class="text-gray-600">Baths</span>
            </div> 
            <div class="flex flex-col items-center">
              <span class="text-2xl font-bold">1,868</span>
              <span class="text-gray-600">Sqft</span>
            </div> 
          </div>
    
          <!-- Price and Revenue -->
          <div class="flex flex-col sm:flex-row sm:justify-between w-full mb-4">
            <p class="text-xl font-bold">$1,650,000</p>
            <p class="text-xl text-gray-600">Revenu générés</p>
          </div>
    
          <!-- Agent Profile -->
          <div class="flex flex-col items-center mb-8">
            <img 
              src="@/assets/images/antoine.jpg"
              alt="Agent Image" 
              class="w-24 h-24 sm:w-32 sm:h-32 rounded-full mb-4"
            />
            <p class="text-sm font-bold text-center">Antoine Blanco</p>
          </div>
    
          <!-- Appointment Button -->
          <button 
            class="w-full bg-black text-white py-3 rounded-full hover:bg-gray-800 transition">
            Prendre un rendez-vous
          </button>
          <p class="text-xs text-gray-500 mt-2 text-center">Earliest at 11:00 tomorrow</p>
        </div>
      </div>
    </section>
    

    <Sponsors/>
    <MainSection/>
  </main>
</template>