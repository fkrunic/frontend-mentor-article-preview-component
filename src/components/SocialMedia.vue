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
            <svg xmlns="http://www.w3.org/2000/svg" width="15" height="13">
                <path fill="#6E8098" d="M15 6.495L8.766.014V3.88H7.441C3.33 3.88 0 7.039 0 10.936v2.049l.589-.612C2.59 10.294 5.422 9.11 8.39 9.11h.375v3.867L15 6.495z"/>
            </svg>
        </div>
    </div>
</template>

<style scoped>
* {
    box-sizing: border-box;
}
</style>