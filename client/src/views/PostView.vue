<script setup>
import { ref } from 'vue'
import { useRoute } from 'vue-router'
const route = useRoute()
const id = parseInt(route.params.id)


fetch('https://dummyjson.com/post/'+id)
.then(res => res.json())
.then(res => post.value = res)

const post = ref()

</script>

<template>
<div class="post">
    <h1>{{ post.title }}</h1>
    <p>{{ post.body }}</p>
</div>
  
</template>



<style scoped>
.post {
    background-color: brown;
    color: wheat;
    padding: 10px 0;
}

img {
    width: 100%;
    height: 300px;
    object-fit: cover;
}
</style>