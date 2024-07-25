<script setup>
import { reactive, ref } from 'vue'
let count = ref(0)
let username = ref('')

let usersList = ref(['Emmanuel', 'Ben', 'James', 'John'])

let usersInfo = ref({ name: 'Alex', age: 20, location: ['NYC', 'IDK'], isMarried: false })

let friends = reactive([ref('Samuel'), ref('Lovia'), ref('Lala')])
</script>

<template>
  <h1>Count: {{ count }}</h1>
  <button @click="count++">+</button>
  <button @click="count--">-</button>

  <h1>Username: {{ username }}</h1>
  <button @click="username = 'Jordan'">Add User</button>

  <h1>Users List: {{ usersList }}</h1>
  <button @click="usersList.push('Doe')">Add User</button>

  <h1>Name: {{ usersInfo.name }}</h1>
  <h1>Age: {{ usersInfo.age }}</h1>
  <h1>Location: {{ usersInfo.location }}</h1>
  <h1>Is Married: {{ usersInfo.isMarried }}</h1>

  <button @click="usersInfo.name = 'Gloria'">Change Name</button>
  <button @click="usersInfo.age = 22">Change Age</button>
  <button @click="usersInfo.location = ['Earth', 'IDK']">Change Location</button>
  <button @click="usersInfo.isMarried = true">Change Status</button>

  <h1>1. {{ friends[0] }}</h1>
  <h1>2. {{ friends[1] }}</h1>
  <h1>3. {{ friends[2] }}</h1>

  <button @click="friends[0] = '🤝'">Hand Shake</button>
  <button @click="friends[1] = '🤝'">Hand Shake</button>
  <button @click="friends[2] = '🤝'">Hand Shake</button>
</template>
