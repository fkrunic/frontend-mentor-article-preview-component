<script setup lang="ts">
import Avatar from '../common/Avatar.vue'
import ShareIcon from '../common/ShareIcon.vue'
defineProps<{ callout: string, bodyText: string }>()
</script>

<template>
    <div class="flex items-center justify-center min-h-screen">
        <div class="flex flex-row w-[45rem] bg-white rounded-xl shadow-lg">
            <img class="w-[18rem] rounded-l-xl" src="../../assets/drawers-desktop.jpg" alt="drawers">
            <div class="flex flex-col gap-6 px-8 py-6">
                <p class="text-xl text-very-dark-gray-blue font-bold">{{ callout }}</p>
                <p class="text-sm text-grayish-blue">{{ bodyText }}</p>
                <div class="flex flex-row justify-between items-center">
                    <Avatar></Avatar>
                    <ShareIcon></ShareIcon>
                </div>
            </div>
        </div>
    </div>
</template>
