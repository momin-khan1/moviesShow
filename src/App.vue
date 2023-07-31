<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
   

      <nav class="flex justify-center font-semibold text-xl">
        <RouterLink class="mr-[40px] hover:text-blue-400" to="/">Home</RouterLink>
        <RouterLink class="mr-[40px] hover:text-blue-400" to="/about">About</RouterLink>
        <RouterLink class="mr-[40px] hover:text-blue-400" to="/movies">Movies</RouterLink>
      </nav>
  

  <RouterView />
</template>

<style scoped>
</style>
