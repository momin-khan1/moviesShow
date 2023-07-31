<script setup>
import { ref, reactive, onMounted } from 'vue'
import MovieCard from '../components/MovieCard.vue'

let movieList = reactive([])
let isLoading = ref(true)

onMounted(() => {
  fetch('http://localhost:3000/movies')
    .then((res) => res.json())
    .then((data) => {
      movieList = data
      isLoading.value = false
      console.log(movieList)
    })
    .catch((error) => console.error('Error Occure', error))
})
</script>

<template>
  <h1 v-if="isLoading"></h1>
  <div v-else class="container mx-auto grid grid-cols-3">
    <MovieCard
        v-for="movie in movieList"
        :key="movie.id"
        :movie = "movie" 
    />
  </div>
</template>

<style scoped></style>
