<script setup>
import { ref, watch } from 'vue'

const username = ref('Jordan')
const counter = ref(0)

watch([username, counter], (newVal, oldVal) => {
  console.log('New Value', newVal)
  console.log('Old Value', oldVal)
})
</script>

<template>
  <h1>{{ username }}</h1>
  <h1>Count: {{ counter }}</h1>

  <button @click="username = 'Ria'">Change Name</button>
  <button @click="counter++">Increment Coounter</button>
  <button @click="counter--">Decrement Coounter</button>
</template>
