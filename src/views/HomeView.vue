

<template>
<div class="home">
  <div>
    <h2 ref="appTitleRef">{{ appTitle }}</h2>
    <h3>{{ counterData.Title }} :</h3>
    <button @click="decrementComuter(2)"  class="btn">-</button>
    <span class="counter">{{ counterData.counter}}</span>
    <button @click="incrementCounter(2)" class="btn">+</button>
  </div>
  <p>This counter is {{oddorEven}}</p>

  <div class="edit">
    <h4>edit counter tilte</h4>
    <input v-model="counterData.Title" type="text" v-autofocus>
  </div>

</div>
</template>

<script setup>

import { reactive,computed, watch, ref} from 'vue';
import {vAutofocus} from '@/directives/vAutofocus.js'

const appTitle = 'Vue 3 Composition API counter app'
const appTitleRef  =  ref(null)


const counterData =  reactive({
  counter: 0,
  Title: 'My Counter title'
})

watch(() => counterData.counter,  (newCount) => {
if (newCount === 10) {
  alert('counter is 10')
}
  
}) 

const oddorEven  = computed(() => {
  return counterData.counter % 2 === 0 ? 'even' : 'odd'
})

const incrementCounter =  amount  => { 
  counterData.counter += amount}
const decrementComuter = amount => {
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