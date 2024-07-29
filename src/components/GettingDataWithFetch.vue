<script setup>
import { ref } from 'vue'

const data = ref(null)

const fetchData = () => {
  //Make a GET request using fetch
  fetch('https://jsonplaceholder.typicode.com/posts')
    .then((response) => {
      //Check if the response status is OK (200-299 range)
      if (!response.ok) {
        throw new Error(`HTTP Error! Status: ${response.status}`)
      }
      //Parse the JSON response
      return response.json()
    })
    .then((responseData) => {
      data.value = responseData
    })
    .catch((error) => {
      console.error(`Error fetching data: ${error}`)
    })
}
</script>

<template>
  <div>
    <h1>((Using Fetch))</h1>
    <button @click="fetchData">Fetch Data</button>

    <div>
      <h2>Data from API:</h2>
      <pre>{{ data }}</pre>
    </div>
  </div>
</template>
