<!-- eslint-disable vue/no-parsing-error -->


<template>
  <div class="posts">
    <h1>Posts</h1>

    <ul>
      <li>
        <RouterLink to="/postsDetail/id1">Post 1</RouterLink>
      </li>
      <li>
        <RouterLink to="/postsDetail/id2">Post 2</RouterLink>
      </li>
      <li>
         <RouterLink to="/postsDetail/id3">Post 3</RouterLink>
      </li>
      <li>
         <RouterLink to="/postsDetail/id4">Post 4</RouterLink>
      </li>
    </ul>

    <textarea v-autofocus></textarea>
  </div>
  </template>

  <script setup>

import {vAutofocus} from '@/directives/vAutofocus.js'
import { RouterLink } from 'vue-router';


</script>
  

<style  scoped>
ul {
  margin-bottom: 30px;
}
</style>