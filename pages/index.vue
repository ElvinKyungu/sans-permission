<script setup lang="ts">

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
    <div class="relative w-full h-[90vh] overflow-hidden">
      <video
        ref="videoRef"
        class="absolute top-0 left-0 w-full h-full object-cover"
        :muted="isMuted"
        autoplay
        loop
        playsinline
      >
        <source src="@/assets/videos/intro.mp4" type="video/mp4" />
        Votre navigateur ne supporte pas la vidéo.
      </video>
      <div class="absolute inset-0 bg-black/50"></div>
      <button
        @click="toggleMute"
        class="absolute bottom-8 right-8 bg-white/90 text-black px-4 py-2 rounded-lg shadow-lg hover:bg-white transition"
      >
        {{ isMuted ? 'Activer le son' : 'Couper le son' }}
      </button>
    </div>
    <MainSection/>
  </main>
</template>