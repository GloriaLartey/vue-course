<script setup>
import { ref, computed } from 'vue'
const number = ref(5)

const squaredNumber = computed(() => {
  return number.value * number.value
})

const firstName = ref('Ria')
const lastName = ref('Lartey')

const fullName = computed(() => firstName.value + ' ' + lastName.value)

const counter = ref(0)
const squaredCounter = computed(() => counter, counter.value ** 2)
const incrementCounter = () => {
  counter.value++
}
</script>

<template>
  <h1>Original Number: {{ number }}</h1>
  <h1>Square Number: {{ squaredNumber }}</h1>

  <h1>Full Name: {{ fullName }}</h1>

  <h1>Counter: {{ counter }}</h1>
  <p>Squared Counter: {{ squaredCounter }}</p>
  <button @click="incrementCounter">Increment Counter</button>
</template>
