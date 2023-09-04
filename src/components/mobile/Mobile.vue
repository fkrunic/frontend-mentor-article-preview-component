<script setup lang="ts">
import InlineSocialMedia from './InlineSocialMedia.vue'
defineProps<{ callout: string, bodyText: string }>()
</script>

<template>
    <div class="flex items-center justify-center min-h-screen">
        <div class="flex flex-col m-6 rounded-xl shadow-xl bg-white">
            <img class="rounded-t-xl" src="../../assets/drawers-mobile.jpg" alt="drawers">
            <div class="flex flex-col pt-8 gap-4">
                <p class="px-8 font-bold text-very-dark-gray-blue">{{ callout }}</p>
                <p class="px-8 pr-6 text-xs leading-5 text-grayish-blue">{{ bodyText }}</p>
                <InlineSocialMedia></InlineSocialMedia>
            </div>
        </div>
    </div>
</template>