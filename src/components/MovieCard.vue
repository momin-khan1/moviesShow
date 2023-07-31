<script setup>
import {defineProps} from 'vue'

defineProps({
    movie: Object
})

</script>

<template>
    <div class="card mt-10 w-96 bg-base-100 shadow-md">
  <figure class="px-10 pt-10 mb-5">
    <img :src="movie.poster" alt="Shoes" class="rounded-xl" />
  </figure>
  <div class="card-body items-center text-center">
    <h2 class="font-bold"> Movice Name: <span class="text-blue-500">{{ movie.title }}</span> </h2>
    <div class="flex justify-center">
        <p class="mr-5"> <span class="text-orange-500">Release Date:</span> {{ movie.year }} </p>
        <p> <span class="text-orange-500">Runtime:</span> {{ movie.runtime }} </p>
    </div>
    <div class="card-actions">
      <button class="bg-blue-500 px-10 py-3 mt-5 mb-10 text-white">See Details</button>
    </div>
  </div>
</div>
</template>

<style scoped></style>