<script setup lang="ts">
import { ref } from 'vue'

const placeholderText = ref('search movies...')
</script>

<template>
  <nav class="nav-bar">
    <div class="logo">
      <span role="img">🍿</span>
      <h1>MovieInfo</h1>
    </div>
    <input class="search" type="text" v-bind:placeholder="placeholderText" />
    <p class="num-results">Found results</p>
  </nav>
</template>

<style src="./PageHeader.style.scss" lang="scss" scoped></style>
