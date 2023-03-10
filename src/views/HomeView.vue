

<template>
<div class="home">
  <div>
    <h2>{{ appTitle }}</h2>
    <h3>{{ counterData.Title }} :</h3>
    <button @click="decrementComuter(2)"  class="btn">-</button>
    <span class="counter">{{ counterData.counter}}</span>
    <button @click="incrementCounter(3)" class="btn">+</button>
  </div>
  <p>This counter is {{oddorEven}}</p>

  <div class="edit">
    <h4>edit counter tilte</h4>
    <input v-model="counterData.Title" type="text">
  </div>

</div>
</template>

<script setup>

import { reactive,computed } from 'vue';

const appTitle = 'Vue 3 Composition API counter app'

/* const counter = ref(0)
const counterTitle = ref('My Counter')
 */
const counterData =  reactive({
  counter: 0,
  Title: 'My Counter title'
})

const oddorEven  = computed(() => {
  return counterData.counter % 2 === 0 ? 'even' : 'odd'
})

const incrementCounter =  amount  => { 
  console.log('amount',amount);
  counterData.counter += amount}
const decrementComuter = amount => {
  console.log('amount',amount);
  counterData.counter-= amount
}
</script>

<style>
.home {
  text-align: center;
  padding: 20px;
}
.btn, .counter {
  font-size: 2rem;
  padding: 0 1rem;
}
.edit {
  margin-top: 60px;
}

</style>