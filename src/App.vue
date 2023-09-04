<script setup lang="ts">
import Mobile from './components/mobile/Mobile.vue'

const content = {
  callout: 'Shift the overall look and feel by adding these wonderful touches to furniture in your home',
  bodyText: [
    'Ever been in a room and felt like something was missing?',
    'Perhaps it felt slightly bare and uninviting.',
    "I've got some simple tips to help you make any room feel complete."
  ].join(' ')
}
</script>

<template>
  <Mobile 
    class="desktop:hidden"
    :callout="content.callout" 
    :body-text="content.bodyText"
    ></Mobile>
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