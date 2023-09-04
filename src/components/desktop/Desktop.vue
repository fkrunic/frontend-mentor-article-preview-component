<script setup lang="ts">
import { ref } from 'vue';
import Avatar from '../common/Avatar.vue'
import ShareIcon from '../common/ShareIcon.vue'
defineProps<{ callout: string, bodyText: string }>()

const showShareMenu = ref(false)

const handleClick = (): void => {
    showShareMenu.value = !showShareMenu.value
}
</script>

<template>
    <div class="flex items-center justify-center min-h-screen">
        <div class="flex flex-row w-[45rem] bg-white rounded-xl shadow-lg">
            <img class="w-[18rem] rounded-l-xl" src="../../assets/drawers-desktop.jpg" alt="drawers">
            <div class="flex flex-col gap-6 px-8 py-6">
                <p class="text-xl text-very-dark-gray-blue font-bold">{{ callout }}</p>
                <p class="text-sm text-grayish-blue">{{ bodyText }}</p>
                <div class="relative flex flex-row justify-between items-center overflow-visible">
                    <Avatar></Avatar>
                    <ShareIcon @click="handleClick"></ShareIcon>

                    <!-- Social Media -->
                    <div class="absolute bg-very-dark-gray-blue p-4 w-[15rem] bottom-[4rem] left-[14.5rem] rounded-xl shadow-lg" 
                        :class="showShareMenu ? '' : 'hidden'">
                        <div class="absolute bg-very-dark-gray-blue w-4 h-4 top-11 left-28 rotate-45"></div>
                        <div class="flex flex-row items-center justify-center gap-4">
                            <p class="text-grayish-blue/75 text-xs tracking-[0.5rem]">SHARE</p>
                            <img class="hover:cursor-pointer" src="../../assets/icon-facebook.svg" alt="share-facebook">
                            <img class="hover:cursor-pointer" src="../../assets/icon-twitter.svg" alt="share-twitter">                
                            <img class="hover:cursor-pointer" src="../../assets/icon-pinterest.svg" alt="share-pinterest">            
                        </div>
                    </div>                    
                </div>
            </div>
        </div>
    </div>
</template>
