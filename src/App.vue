<script setup lang="ts">
import { RouterView } from 'vue-router'
</script>

<template>
  <div class="container">
    <nav>
      <RouterLink :to="{ name: 'home', query: { bar: 'poop' } }">Home</RouterLink>
      <RouterLink :to="{ name: 'about' }">About</RouterLink>
    </nav>
    <br />
    <RouterView />
  </div>
</template>

<style scoped>
.container {
  display: flex;
  flex-direction: column;
  height: 100vh;
  width: 100%;
  background-color: blue;
}
nav {
  /* margin: 8px; */
  background-color: magenta;
}
</style>
