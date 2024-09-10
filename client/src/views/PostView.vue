<template>
    <article>
        {{ post.body }}
    </article>
  
</template>

<script setup>
import { ref } from "vue";
import CardPostView from "./CardPostView.vue";

import { } from 'vue'



const index = ref(1)
const post = ref([])

fetch('http://dummyjson.com/posts/')
    .then(res = res.json())
    .then(res => {
        post.value = res
    })
</script>