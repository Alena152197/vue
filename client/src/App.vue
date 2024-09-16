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
          <RouterLink to="/contact">Contacts</RouterLink>
        </nav>

      </header>
    </div>
  </header>




  <main class="container mx-auto">
    <RouterView />
  </main>

  <section>
    <ShareView />
  </section>

  <footer class="container mx-auto ">
    все права защищены &copy; 2024
  </footer>


 

</template>

<style scoped>
section {
  position: fixed;
  bottom: 60px;
  right: 100px;
}

nav {
  background-color: wheat;
}

a {
  border: 1px solid brown;
  border-radius: 5px;
  padding: 5px;
  background: brown;
  color: wheat;
  
}
</style>