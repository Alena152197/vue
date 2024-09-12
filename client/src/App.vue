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
    все права защищены &copy; 2024
  </footer>


</template>

<style scoped>
nav {
  background-color: wheat;
  
}
</style>
