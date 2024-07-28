<script setup>
import { reactive, watch } from 'vue'

const state = reactive({ username: 'alex' })

//Here we can't provide specific property of object
//-we have to provide the entire object, otherwise it's gonna give us error in the console

// watch(state.username, (newValue, oldValue) => {
//   console.log('new value', newValue)
//   console.log('old value', oldValue)
// })

//if we're using 'object' both the new and old values will be the same

// watch(state, (newValue, oldValue) => {
//   console.log('new value', newValue)
//   console.log('old value', oldValue)
// })

//Now if we want to get the 'old and 'new values seperately,
//-for thta we'll have to pass a getter function.
//-And here we have to specify the actual object/state 'property'.

watch(
  () => state.username,
  (newValue, oldValue) => {
    console.log('new value', newValue)
    console.log('old value', oldValue)
  }
)
</script>

<template>
  <h1>{{ state.username }}</h1>
  <button @click="state.username = Jordan">Change Name</button>
</template>
