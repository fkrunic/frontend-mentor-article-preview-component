<script setup lang="ts">
import SocialMedia from './components/SocialMedia.vue'
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

      desktop:flex-row
      desktop:h-[18rem]
      desktop:w-[50rem]
    ">

      <!-- Drawers-->
      <div class="
        relative 
        h-0 
        pb-[65%] 
        overflow-hidden
        ">
        <img class="
          absolute 
          rounded-t-xl
          
          desktop:static
          desktop:rounded-none
          desktop:w-[50.5rem]
          desktop:rounded-l-xl
          " src="./assets/drawers.jpg" alt="drawers">
      </div>      

      <!-- Callout -->
      <div class="
        flex 
        flex-col 
        pt-8 
        gap-4
        
        desktop:w-[61rem]
        desktop:pl-2
        ">
        <p class="
          px-8 
          font-bold 
          text-very-dark-gray-blue
          
          desktop:text-xl
          ">
          Shift the overall look and feel by adding these wonderful touches 
          to furniture in your home
        </p>

        <p class="
          px-8 
          pr-6 
          text-xs 
          leading-5 
          
          text-grayish-blue
          desktop:leading-5
          ">
          Ever been in a room and felt like something was missing? Perhaps it
          felt slightly bare and uninviting. I've got some simple tips to help 
          you make any room feel complete.
        </p>
        <SocialMedia></SocialMedia>
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