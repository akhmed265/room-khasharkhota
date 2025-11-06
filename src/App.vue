<template>
  <div id="app">
    <Start />
    <About />
    <Offer />
    <Popular />
  </div>
</template>

<script setup lang="ts">
  import Start from './sections/Start.vue'
  import About from './sections/About.vue'
  import Offer from './sections/Offer.vue'
  import Popular from './sections/Popular.vue'

</script>
<style lang="scss">
  * {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
  }
</style>
