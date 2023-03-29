<!-- eslint-disable vue/no-parsing-error -->


<template>
  <div class="posts">
    <h1>Posts</h1>

    <ul>
      <li  v-for="post in posts"
      :key="post.id">
        <RouterLink :to="`/postsDetail/${post.id}`">{{ post.title}}</RouterLink>
      </li>
  
    </ul>

    <textarea v-autofocus></textarea>
  </div>
  </template>

  <script setup>

import {vAutofocus} from '@/directives/vAutofocus.js'
import { ref } from 'vue';
import { RouterLink } from 'vue-router';


const posts =  ref([
  {
    id: 'id1',
    title: 'Post 1'
  },
  {
    id: 'id2',
    title: 'Post 2'
  },
  {
    id: 'id3',
    title: 'Post 3'
  },
  {
    id: 'id4',
    title: 'Post 4'
  }
])

</script>
  

<style  scoped>
ul {
  margin-bottom: 30px;
}
</style>