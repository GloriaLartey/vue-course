<script setup>
import { ref } from 'vue'
let count = ref(0)
const incrementCounter = () => count.value++
const decrementCounter = () => count.value--

const submitHandler = (e) => {
  e.preventDefault()
  alert('Valid Credentials')
}

const showMessage = (message) => alert(message)
</script>

<template>
  <h1>Count: {{ count }}</h1>
  <button @click="incrementCounter" class="b-in">Increment</button>
  <button @click="decrementCounter" class="b-de">Decrement</button>

  <form @:submit="submitHandler">
    <div>Name:</div>
    <input type="text" placeholder="Please enter your name" /> <br />
    <br />
    <div>Email:</div>
    <input type="email" placeholder="Please enter your email" /><br />
    <button type="submit" class="submit">Submit</button>

    <button @click="showMessage('this is my message')" class="show">Show Message</button>
  </form>
</template>
<style>
.b-in,
.b-de {
  background-color: rgb(235, 225, 217);
  border: none;
  border-radius: 20px;
  padding: 10px;
  font-weight: bold;
  margin-right: 5px;
  margin-bottom: 5px;
}

input {
  padding: 10px;
  font-size: 15px;
}

.submit,
.show {
  background-color: rgb(105, 105, 221);
  border: none;
  margin-right: 10px;
  margin-top: 9px;
  color: white;
  padding: 8px;
  font-size: 14px;
  border-radius: 5px;
}
</style>
