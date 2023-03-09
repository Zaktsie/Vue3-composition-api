

<template>
<div class="home">
  <div>
    <h3>{{ counterTitle }} :</h3>
    <button @click="decrement"  class="btn">-</button>
    <span class="counter">{{ counter}}</span>
    <button @click="increment" class="btn">+</button>
  </div>
</div>
</template>

<script setup>

import { ref } from 'vue';


const counter = ref(0)
const counterTitle = ref('My Counter')
const increment = () => counter.value++
const decrement = () => counter.value--

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