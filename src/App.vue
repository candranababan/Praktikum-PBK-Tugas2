<script setup>
import { reactive, ref } from 'vue'

const awesome = ref(true) 
const count = ref(0)
const text = ref('')


function increment(){
  count.value++
}

function saya() {
  awesome.value = !awesome.value
}


</script>

<template>
  <input v-model="text" placeholder="type here">
    <p>{{ text }}</p>
      <button @click="saya">saya</button>
      <button @click="increment">tekan: {{ count }}</button>
    <h1 v-if="awesome">saya benar</h1>
    <h1 v-else>saya salah</h1>
</template>

