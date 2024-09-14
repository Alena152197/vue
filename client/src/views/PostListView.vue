<script setup>
import CardPostView from './CardPostView.vue';
import PostListView from './PostListView.vue';
import PostView from './PostView.vue';

import { ref } from 'vue'
fetch('https://dummyjson.com/posts/')
.then(res => res.json())
.then(res => posts.value = res.posts)

const posts = ref()

</script>

<template>
    <ul>
        <CardPostView></CardPostView>
    </ul>

    <PostListView></PostListView>
</template>




<style scoped>
ul {
    display: grid;
    grid-template-columns: repeat();
}
</style>
