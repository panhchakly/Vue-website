<script setup lang="ts">
import Navbar from './components/Navbar.vue'
import Banner from './components/Banner.vue'
import Promotion from './components/Promotion.vue'
import Category from './components/Category.vue'
import Footer from './components/Footer.vue'
</script>

<template>
  <div class="app">
    <Navbar />
    <Banner />
    <Promotion />
    <Category />
    <Footer />
  </div>
</template>

<style scoped>
.app {
  min-height: 100vh;
}
</style>
