<script setup lang="ts">
import InlineSocialMedia from './InlineSocialMedia.vue'
</script>

<template>
  <div class="flex items-center justify-center min-h-screen">

    <!-- Card -->
    <div class="flex flex-col m-6 rounded-xl shadow-xl bg-white">

      <!-- Drawers-->
      <div class="relative h-0 pb-[65%] overflow-hidden">
        <img class="absolute rounded-t-xl" src="../../assets/drawers.jpg" alt="drawers">
      </div>      

      <!-- Callout -->
      <div class="flex flex-col pt-8 gap-4">
        <p class="px-8 font-bold text-very-dark-gray-blue">
          Shift the overall look and feel by adding these wonderful touches 
          to furniture in your home
        </p>

        <p class="px-8 pr-6 text-xs leading-5 text-grayish-blue">
          Ever been in a room and felt like something was missing? Perhaps it
          felt slightly bare and uninviting. I've got some simple tips to help 
          you make any room feel complete.
        </p>
        <InlineSocialMedia></InlineSocialMedia>
      </div>
    </div>
  </div>
</template>

<style scoped>
* {
  box-sizing: border-box;
}
</style>