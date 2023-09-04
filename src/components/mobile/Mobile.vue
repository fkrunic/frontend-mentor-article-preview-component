<script setup lang="ts">
import { ref } from 'vue';
import ShareIcon from '../common/ShareIcon.vue'
import Avatar from '../common/Avatar.vue'
defineProps<{ callout: string, bodyText: string }>()

const showShareMenu = ref(false)

const handleClick = (): void => {
    showShareMenu.value = !showShareMenu.value
}
</script>

<template>
    <div class="flex items-center justify-center min-h-screen">
        <div class="flex flex-col m-6 rounded-xl shadow-xl bg-white">
            <img class="rounded-t-xl" src="../../assets/drawers-mobile.jpg" alt="drawers">
            <div class="flex flex-col pt-8 gap-4">
                <p class="px-8 font-bold text-very-dark-gray-blue">{{ callout }}</p>
                <p class="px-8 pr-6 text-xs leading-5 text-grayish-blue">{{ bodyText }}</p>

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

                    <Avatar :class="showShareMenu ? 'hidden': ''"></Avatar>
                    <ShareIcon @click="handleClick"></ShareIcon>
                </div>

            </div>            
        </div>
    </div>
</template>