<template>
  <div id="app">
    <Start />

    <About />
  </div>
</template>

<script setup lang="ts">
  import Start from './sections/Start.vue'
  import About from './sections/About.vue'

</script>
<style lang="scss">
  * {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
  }
</style>
