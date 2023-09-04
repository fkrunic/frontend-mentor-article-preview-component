<script setup lang="ts">
defineProps<{ callout: string, bodyText: string }>()
</script>

<template>
    <div class="flex items-center justify-center min-h-screen">
        <div class="flex flex-row w-[60rem] bg-white rounded-xl shadow-lg">
            <img class="w-[18rem] rounded-l-xl" src="../../assets/drawers-desktop.jpg" alt="drawers">
            <div class="flex flex-col">
                <p class="text-xl text-very-dark-gray-blue font-bold">{{ callout }}</p>
                <p class="text-sm text-grayish-blue">{{ bodyText }}</p>
            </div>
        </div>
    </div>
</template>

<style scoped>
* {
    box-sizing: border-box;
}
</style>