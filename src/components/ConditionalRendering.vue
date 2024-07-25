<script setup>
import { ref } from 'vue'

const isTrue = true
const isFalse = false

let isVisible = ref(true)

let isUserLoggedIn = ref(true)
let username = 'Ria'
let showDetails = ref(isUserLoggedIn)

const isActive = ref(true)

let password = ref('mypersonalpassword')
</script>

<template>
  <div>
    <p v-if="isTrue">This will show if isTrue is true.</p>
    <p v-else-if="isFalse">This will show if isFalse is true.</p>
    <p v-else>This will show if neither isTrue nor isFalse is true</p>
  </div>
  <!-- v-show -->
  <p v-show="isVisible">This paragragh will be shown or hidden based on the value of isVisible</p>
  <button @click="isVisible = !isVisible">Toggle Visibility</button>

  <div>
    <h1 v-if="isUserLoggedIn">Welcome, {{ username }}</h1>
    <p v-else>Please log in to access this content.</p>

    <div v-show="showDetails">
      <h4>You're now able to modify your dashboard</h4>
    </div>
  </div>

  <div v-if="isActive">
    <h1>My Blog Post</h1>
    <p>
      Lorem ipsum dolor sit amet npconsectetur adipisicing elit. Eligendi veritatis sunt culpa
      voluptatem debitis expedita quas ea, nisi mollitia consectetur ab officia architecto quis
      perferendis voluptates amet saepe. Odio, rem.
    </p>
  </div>

  <button @click="isActive = !isActive">Toggle Post</button>

  <h1 v-if="password.length > 8">Strong Password</h1>
  <h1 v-else-if="password.length < 8">Weak Password</h1>
  <h1 v-else>Please Enter Your Password</h1>
</template>
