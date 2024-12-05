<script setup lang="ts">
import gsap from 'gsap'
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
      <div class="screen-container">
        <div 
          class="bg relative"
        >
          <img 
            src="https://blogdoiphone.com/wp-content/uploads/2024/06/iOS-18-Wallpaper-ac.jpeg" 
            class="absolute h-full w-full inset-0 object-cover z-5" 
            alt="" 
            srcset=""
          >
          <div class="notch-container">
            <div class="notch">
              <div class="content">
                <div class="left">
                  <!-- <div class="tile"></div> -->
                   <img src="@/assets/images/channels4_profile.jpg" class="w-20 h-20" alt="">
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
            <div class="mt-4 mr-5 flex justify-end space-x-3 z-50">
              <IconNetwork/>
              <IconWifi />
              <IconBattery />
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</div>
</template>