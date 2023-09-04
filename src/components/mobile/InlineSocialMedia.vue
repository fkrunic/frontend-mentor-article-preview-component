<script setup lang="ts">
import { ref } from 'vue';
import ShareIcon from '../common/ShareIcon.vue'

const showShareMenu = ref(false)

const handleClick = (): void => {
    showShareMenu.value = !showShareMenu.value
}
</script>

<template>

    <!-- Author variant -->
    <div class="
        flex 
        flex-row 
        items-center 
        justify-between 

        h-16
        p-8
        
        rounded-b-xl
        "
        :class="showShareMenu ? 'bg-very-dark-gray-blue' : ''"
        >

        <!-- Social Media -->
        <div :class="showShareMenu ? '' : 'hidden'">
            <div class="flex flex-row items-center justify-center gap-4">
                <p class="text-grayish-blue/75 text-xs tracking-[0.5rem]">SHARE</p>
                <img class="hover:cursor-pointer" src="../../assets/icon-facebook.svg" alt="share-facebook">
                <img class="hover:cursor-pointer" src="../../assets/icon-twitter.svg" alt="share-twitter">                
                <img class="hover:cursor-pointer" src="../../assets/icon-pinterest.svg" alt="share-pinterest">            
            </div>
        </div>

        <!-- Avatar -->
        <div 
            class="flex flex-row items-center gap-4 mb-4"
            :class="showShareMenu ? 'hidden': ''"
            >
            <img class="w-10 h-10 rounded-full" src="../../assets/avatar-michelle.jpg" alt="michelle">
            <div class="flex flex-col gap-1">
                <p class="font-bold text-xs text-very-dark-gray-blue">
                    Michelle Appleton
                </p>
                <p class="text-xs text-grayish-blue">
                    28 Jun 2020
                </p>
            </div>
        </div>

        <!-- Icon Container -->
        <div class="">
            <ShareIcon @clicked="handleClick"></ShareIcon>
        </div>
    
    </div>
</template>

<style scoped>
* {
    box-sizing: border-box;
}
</style>