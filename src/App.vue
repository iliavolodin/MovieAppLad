<script setup lang="ts">
// import { RouterLink, RouterView } from 'vue-router'
import PageFooter from './components/Footer/PageFooter.vue'
import PageHeader from './components/Header/PageHeader.vue'
import MainBox from './components/UI/BoxMovies/BoxMovies.vue'
</script>

<template>
  <div class="wrapper">
    <PageHeader />
    <MainBox />
    <PageFooter />
  </div>
</template>

<style scoped>
.wrapper {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  min-height: 100vh;
}
</style>
