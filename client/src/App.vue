<script setup>
  import { RouterLink, RouterView } from 'vue-router'
  import ShareView from './views/ShareView.vue';
</script>

<template>
  <header>
    <div id="minApp" class="container mx-auto">
      <header class="bg-teal-400">

        <nav class="flex flex-row p-5 gap-5 text-lg font-bold">
          <RouterLink to="/">Home</RouterLink>
          <RouterLink to="/about">About</RouterLink>
          <RouterLink to="/blog">Blog</RouterLink>

        </nav>

      </header>
    </div>
  </header>




  <main>
    <RouterView />
  </main>

  <section>
    <ShareView />
  </section>

  <footer>
    все права защищены &copy; 2024
  </footer>


 

</template>

<style scoped>
section {
  position: fixed;
  bottom: 60px;
  right: 60px;
}

nav {
  background-color: wheat;
}
</style>