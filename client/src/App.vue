<script setup>
import { RouterLink, RouterView } from 'vue-router'

</script>

<template>
  <header>

    <nav>
      <RouterLink to="/">Home</RouterLink>
      <RouterLink to="/about">About</RouterLink>
      <RouterLink to="/blog">Blog</RouterLink>
    </nav>

  </header>



  <main>
    <RouterView />
  </main>

  <footer>

  </footer>


</template>

<style scoped>
nav {
  display: flex;
  gap: 10px;

}
</style>
