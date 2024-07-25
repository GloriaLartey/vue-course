<script setup>
import { reactive } from 'vue'
let initialState = reactive({ count: 0 })
let initialStates = reactive({ val: { count: 0 }, user: ['Gloria', 'Lovia'] })

const changeUser = () => {
  initialStates.user[0] = 'Daniel'
  initialStates.user[1] = 'Benjamin'
}
</script>

<template>
  <h1>Count: {{ initialState.count }}</h1>
  <button @click="initialState.count++">+</button>
  <button @click="initialState.count--">-</button>

  <h1>Current Count: {{ initialStates.val.count }}</h1>
  <h2>User: {{ initialStates.user }}</h2>

  <button @click="initialStates.val.count += 10">Add 10</button>
  <button @click="changeUser">Change User</button>
  <button @click="initialStates.user.push('SOD')">Add One More</button>
</template>
