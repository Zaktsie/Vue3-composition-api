

<template>
<div class="home">
  <div>
    <h2>{{ appTitle }}</h2>
    <h3>{{ counterData.Title }} :</h3>
    <button @click="decrement"  class="btn">-</button>
    <span class="counter">{{ counterData.counter}}</span>
    <button @click="increment" class="btn">+</button>
  </div>
</div>
</template>

<script setup>

import { reactive } from 'vue';

const appTitle = 'Vue 3 Composition API counter app'

/* const counter = ref(0)
const counterTitle = ref('My Counter')
 */
const counterData =  reactive({
  counter: 0,
  Title: 'My Counter title'
})
const increment = () => counterData.value++
const decrement = () => counterData.value--

</script>


<!-- 
Composition API example
<script>
import {ref } from 'vue';
export default { 
  setup() {
    const counter = ref(20)
 
 
 return {
  counter,
  increment() {
    counter.value++
  },
  decrement() {
    counter.value--
  },
 }
  }
}

</script> -->

<!-- options API example  -->

<!-- <script>
export default {
 data ()  {
  return {
  counter : 0
 } 
},
methods: {
  increment() {
    this.counter++
  },
  decrement() {
    this.counter--
  },
  
},
}

  </script> -->


<style>
.home {
  text-align: center;
  padding: 20px;
}
.btn, .counter {
  font-size: 2rem;
  padding: 0 1rem;
}


</style>