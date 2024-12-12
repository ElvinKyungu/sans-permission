<script setup lang="ts">
import gsap from "gsap";

onMounted(() => {
  const timeline = gsap.timeline();

  // Animation pour la première carte
  timeline
    .fromTo(
      ".card-1",
      {
        x: "100%",   // Commence à droite
        opacity: 0,
        scale: 0.8,
      },
      {
        x: "50%",    // Se déplace vers le centre
        opacity: 1,
        scale: 1,
        duration: 1,
      }
    )
    // Animation pour la deuxième carte
    .fromTo(
      ".card-2",
      {
        x: "100%",   // Commence à droite
        opacity: 0,
        scale: 0.8,
      },
      {
        x: "50%",    // Se déplace vers le centre
        opacity: 1,
        scale: 1,
        duration: 1,
      },
      "-=0.5" // La deuxième carte arrive avant que la première ne finisse
    )
    .to(
      ".card-1",
      {
        x: "-50%",
        y: "-10%",
        rotate: -10,
        scale: 0.9,
        duration: 1,
      },
      "-=0.8"
    )
    // Animation pour la troisième carte
    .fromTo(
      ".card-3",
      {
        x: "1250px",   // Commence à droite
        opacity: 0,
        scale: 0.8,
      },
      {
        x: "-50%",    // Se déplace vers le centre
        opacity: 1,
        scale: 1,
        duration: 1,
        rotate: -10,
      },
      "-=0.5"
    )
    .to(
      ".card-2",
      {
        x: "-50%",
        y: "-10%",
        rotate: -10,
        scale: 0.9,
        duration: 1,
      },
      "-=0.8"
    )
    // Superposition finale
    .to(
      [".card-1", ".card-2", ".card-3"],
      {
        y: (i: number) => `${i * 40}%`, // Décalage vertical
        x: "-50%",
        rotate: 0,
        scale: 1,
        duration: 1,
        opacity: 1,
      },
      "+=1"
    );
});
</script>


<template>
  <div class="scene">
    <div class="phone-con">
      <div class="phone">
        <div class="buttons">
          <div class="left">
            <div class="button"></div>
            <div class="button"></div>
            <div class="button"></div>
          </div>
          <div class="right">
            <div class="button"></div>
          </div>
        </div>
        <div class="screen-container relative">
          <div class="bg relative">
            <img
              src="https://blogdoiphone.com/wp-content/uploads/2024/06/iOS-18-Wallpaper-ac.jpeg"
              class="absolute h-full w-full inset-0 object-cover z-5"
              alt=""
            />
            <div class="notch-container">
              <div class="notch">
                <div class="content">
                  <div class="left">
                    <img
                      src="@/assets/images/channels4_profile.jpg"
                      class="w-20 h-20"
                      alt=""
                    />
                    <div class="text"></div>
                  </div>
                  <div class="right"></div>
                  <div class="bar">
                    <div class="duration"></div>
                  </div>
                </div>
              </div>
            </div>
            <div class="relative h-full w-full">
              <div class="mt-4 mr-5 flex justify-end items-center space-x-1 z-50">
                <IconsBattery class="w-5 h-5" />
                <IconsWifi class="w-5 h-5" />
                <IconsNetwork class="w-5 h-5" />
              </div>
            </div>
            <div class="cards-container w-80 h-80 absolute z-50">
              <!-- <h1 class="text-6xl font-semibold">Sans permission</h1>
              <h2 class="text-4xl font-medium text-gray-200">1er podcast business</h2> -->
              <!-- Card 1 -->
              <!-- <div
                class="card-1 absolute w-80 h-80 bg-indigo-200 rounded-lg shadow-lg"
              ></div> -->

              <!-- Card 2 -->
              <!-- <div
                class="card-2 absolute w-80 h-64 bg-indigo-300 rounded-lg shadow-lg"
              ></div> -->

              <!-- Card 3 -->
              <!-- <div
                class="card-3 absolute w-80 h-64 bg-indigo-400 rounded-lg shadow-lg"
              >

              </div> -->
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.cards-container {
  perspective: 1000px;
}
.card-1,
.card-2,
.card-3 {
  position: absolute;
  left: 50%;
  transform: translate(-50%);
  opacity: 0;
  top: -10%;
  scale: 0.8;
}
</style>
