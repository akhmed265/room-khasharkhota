<template>
  <div id="app">
    <Start />
    <About />
    <Offer />
    <Popular />
    <Blog />
    <Gallery />
    <Newsletter />
    <Footer />

  </div>
</template>

<script setup lang="ts">
  import Start from './sections/Start.vue'
  import About from './sections/About.vue'
  import Offer from './sections/Offer.vue'
  import Popular from './sections/Popular.vue'
  import Blog from './sections/Blog.vue'
  import Gallery from './sections/Gallery.vue'
  import Newsletter from './sections/Newsletter.vue'
  import Footer from './sections/Footer.vue'

</script>
<style lang="scss">
  * {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
  }
</style>
