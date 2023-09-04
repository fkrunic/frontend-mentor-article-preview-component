<script setup lang="ts">
import Mobile from './components/mobile/Mobile.vue'
</script>

<template>
  <Mobile class="desktop:hidden"></Mobile>
</template>

<script lang="ts">
export default {
  data() {
    return {
      bodyClass: 'font-manrope bg-light-grayish-blue'
    };
  },
  mounted() {
    document.body.className = this.bodyClass;
  },
  beforeDestroy() {
    // Reset the class when the component is destroyed
    document.body.className = '';
  }
};
</script>