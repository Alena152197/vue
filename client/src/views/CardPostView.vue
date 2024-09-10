<template>

        <li v-for="(post, index) in posts" :key="post.id">
            <h3>{{ post }}</h3>
            <ul>
                <li v-for="tag in posts" :key="post">
                    <h3>{{ post }}</h3>
                </li>
            </ul>
        </li>

</template>

<script setup>
import { ref } from "vue"

const title = defineModel('title')
const posts = ref([])

fetch('https://dummyjson.com/posts/'+'')
    .then(res => res.json())
    .then(res => {
        posts.value = res.posts
    })
    .then(console.log);

const posts = []

</script>


