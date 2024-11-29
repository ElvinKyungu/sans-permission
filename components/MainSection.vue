<script setup lang="ts">
import Badge from './icons/Badge.vue';
import type Cursor from './icons/Cursor.vue';
</script>

<template>
  <section class="grid grid-cols-12 min-h-screen px-32 mt-10">
    <div class="col-span-3 bg-indigo-300 relative">
      <div class="flex space-x-4">
        <button class="flex gap-2 items-center py-2 px-5 border rounded-full border-[#18016b]">
          <Badge class="text-green-400"/>
          <span>Business</span>
        </button>
        <button class="flex gap-2 items-center py-2 px-5 border rounded-full border-[#57c049]">
          <IconsCursor/>
          <span>Artificial Intelligente</span>
        </button>
      </div>
      <!-- <div class="text-8xl uppercase text-nowrap">
        <h1 class="">Where your</h1>
        <h1 class="">Mental health</h1>
        <h1 class="flex gap-2">
          <Badge class="w-10 h-10"/>
          <span>Flourishes</span>
        </h1>
      </div> -->
      <div id="outer" class="text-8xl uppercase text-nowrap ">
        <div id="inner-container">
          <div class="innertext"><span>Where your</span></div>
          <div class="innertext"><span>Mental health</span></div>
          <div class="innertext"><span>Flourishes</span></div>
        </div>
      </div>
    </div>
    <div class="col-span-6 bg-slate-200 relative z-10">
      d
    </div>
    <div class="col-span-3 ">
    </div>
  </section>
</template>

<style scoped>
#outer {
  width: 100%;
  height: 400px;
  border-radius: 20px;
   position: relative;
}
#inner-container {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  position: absolute;
  bottom: 0px;
}
.innertext {
  display: inline;
  position: relative;
  border-top-right-radius: 20px;
  background-color: #fff;
  padding: 5px 25px 0px 5px;
  z-index: 99;
  color: #000;
}
.innertext:first-child::before,
.innertext::after {
  content: "";
  display: block;
  width: 40px;    /* double the radius */
  height: 40px;   /* double the radius */
  background-color: transparent;
  position: absolute;
  border-bottom-left-radius: 20px;
  box-shadow: 0 20px 0 0 #fff;  
}
.innertext::before {
  top: -40px;
  left: 0;
}
.innertext::after {
  right: -2.2rem;
  top: 62px;
  z-index: 0 !important;
}
.innertext span {
  position: relative;
  z-index: 1;   /* to overcome the overlapping with the text */
}
</style>