<template>

    <li class="post" v-for="(post, index) in posts" :key="post.id">
        <h3>{{ post.title }}</h3>
        <img src="#" alt="нет обложки">
        <ul class="tags">
            <li class="tag" v-for="tag in post" :key="tag.id">
                {{ tag }}
            </li>
        </ul>
        <RouterLink :to="'/post/' + (index + 1)">Читать подробнее</RouterLink>
    </li>

</template>

<script setup>
import { ref } from 'vue'
const posts = ref([])

fetch('https://dummyjson.com/posts/' + '')
    .then(res => res.json())
    .then(res => posts.value = res.posts)
</script>

<style scoped>
.post li:hover {
    transition: all .1s linear;
    box-shadow: 5px 5px 5px -5px;
    border: 1px solid #000;
    border-color: aqua;
}


.post {
    background-color: wheat;
    color: brown;
    padding: 10px;
    display: flex;
    flex-direction: column;
    gap: 10px;
    justify-content: space-between;
    border: 2px solid #000;

}

h3 {
    height: 50px;
}

.tags {
    display: flex;
    gap: 10px;
}

a {
    padding: 10px;
    background-color: brown;
    text-decoration: none;
    color: wheat;
}

a:hover {
    filter: brightness(1.2);
}
</style>
