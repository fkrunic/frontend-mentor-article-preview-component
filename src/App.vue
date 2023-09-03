<script setup lang="ts">
</script>

<template>
  <div class="flex items-center justify-center min-h-screen">

    <!-- Card -->
    <div class="
      flex
      flex-col

      m-6

      rounded-xl
      shadow-xl
      bg-white
    ">

      <!-- Drawers-->
      <div class="relative h-0 pb-[65%] overflow-hidden">
        <img class="absolute rounded-t-xl" src="./assets/drawers.jpg" alt="drawers">
      </div>      

      <!-- Callout -->
      <div class="flex flex-col p-8 pb-5 gap-4">
        <p class="font-bold text-very-dark-gray-blue">
          Shift the overall look and feel by adding these wonderful touches 
          to furniture in your home
        </p>

        <p class="text-xs leading-5 pr-6 text-grayish-blue">
          Ever been in a room and felt like something was missing? Perhaps it
          felt slightly bare and uninviting. I've got some simple tips to help 
          you make any room feel complete.
        </p>

        <!-- Author -->
        <div class="flex flex-row items-center pt-4 justify-between">

          <!-- Avatar Section -->
          <div class="flex flex-row gap-4 items-center">
            <img class="w-10 h-10 rounded-full" src="./assets/avatar-michelle.jpg" alt="michelle">
            <div class="flex flex-col">
              <p class="font-bold text-xs text-very-dark-gray-blue">
                Michelle Appleton
              </p>
              <p class="text-xs text-grayish-blue">
                28 Jun 2020
              </p>
            </div>
          </div>

          <!-- Share Icon -->
          <div class="flex items-center justify-center w-8 h-8 rounded-full p-2 bg-grayish-blue/25">
            <img src="./assets/icon-share.svg" alt="share">
          </div>      
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
* {
  box-sizing: border-box;
}
</style>

<script lang="ts">
export default {
  data() {
    return {
      bodyClass: 'font-manrope bg-light-grayish-blue'
    };
  },
  mounted() {
    document.body.className = this.bodyClass;
  },
  beforeDestroy() {
    // Reset the class when the component is destroyed
    document.body.className = '';
  }
};
</script>