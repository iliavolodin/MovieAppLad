<script setup lang="ts">
//В этом варианте происходит ошибка. console.log() выдаёт undefined у props.initialMovies.
// const props = defineProps({
//initialMovies:{
//   imdbID: String,
//   Title: {
//     type: String,
//     required: false,
//     default: 'Test'
//   },
//   Year: String,
//   Poster: String
//  }
// })

//Ругается на непредоставление типов, но работает:)
const props = defineProps({
  initialMovies: {}
})

console.log(props.initialMovies)
</script>

<template>
  <li class="item" v-for="movie in initialMovies" :key="movie.imdbID">
    <img class="item_img" :src="movie.Poster" :alt="movie.Title" />
    <h3 class="item_title">{{ movie.Title }}</h3>
    <div class="item_wrapper">
      <p class="list_text">
        <span>Year: {{ movie.Year }} </span>
      </p>
    </div>
  </li>
</template>

<style src="./BoxMovie.style.scss" lang="scss" scoped></style>
