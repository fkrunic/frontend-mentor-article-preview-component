<script setup lang="ts">
</script>

<template>
    <!-- Author -->
    <div class="flex flex-row items-center pt-4 justify-between">

        <!-- Avatar Section -->
        <div class="flex flex-row gap-4 items-center">
            <img class="w-10 h-10 rounded-full" src="../assets/avatar-michelle.jpg" alt="michelle">
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
            <img src="../assets/icon-share.svg" alt="share">
        </div>
    </div>
</template>

<style scoped>
* {
    box-sizing: border-box;
}
</style>