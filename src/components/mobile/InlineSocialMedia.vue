<script setup lang="ts">
import { ref } from 'vue';
import ShareIcon from '../common/ShareIcon.vue'
import Avatar from '../common/Avatar.vue'

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

        <Avatar :class="showShareMenu ? 'hidden': ''"></Avatar>
        <ShareIcon @click="handleClick"></ShareIcon>
    </div>
</template>
