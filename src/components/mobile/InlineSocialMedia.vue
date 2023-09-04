<script setup lang="ts">
import { ref } from 'vue';

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

            <!-- Share Icon -->
            <div 
                class="
                    flex 
                    items-center 
                    justify-center 
                    
                    w-8 
                    h-8 

                    p-2
                    
                    rounded-full  
                    bg-grayish-blue/25

                    group
                    hover:bg-desaturated-dark-blue  
                    hover:cursor-pointer              
                "
                @click="handleClick"
                >
                <svg  
                    class="
                        fill-very-dark-gray-blue/75                
                        group-hover:fill-white
                        "            
                    xmlns="http://www.w3.org/2000/svg" 
                    width="15" 
                    height="13"
                    >
                    <path d="M15 6.495L8.766.014V3.88H7.441C3.33 3.88 0 7.039 0 10.936v2.049l.589-.612C2.59 10.294 5.422 9.11 8.39 9.11h.375v3.867L15 6.495z"/>
                </svg>
            </div>
        </div>
    
    </div>
</template>

<style scoped>
* {
    box-sizing: border-box;
}
</style>