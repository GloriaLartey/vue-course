<!-- JavaScript -->
<script setup>
const myMessage = 'Yellow World'
const myNumber = 100
function add(x, y) {
  return x + y
}

// const myChannel = 'https://www.youtube.com/@hunxwebdev'
// const amazingImage =
//   'https://www.google.com/imgres?q=c%2B%2B%20and%20css%20difference&imgurl=https%3A%2F%2Fstatic.javatpoint.com%2Fcpp%2Fimages%2Fconstructor-vs-destructor-in-cpp.png&imgrefurl=https%3A%2F%2Fwww.javatpoint.com%2Fconstructor-vs-destructor-in-cpp&docid=CV1wKzMSVJQf8M&tbnid=xa7aUJT2-y9xJM&vet=12ahUKEwiog7Sz4rSHAxXyQEEAHeR_DDYQM3oECH8QAA..i&w=560&h=245&hcb=2&ved=2ahUKEwiog7Sz4rSHAxXyQEEAHeR_DDYQM3oECH8QAA'

// const imageWidth = 400
// const imageHeight = 400

//Dynamic Binding
const imageInfo = {
  src: 'https://www.google.com/imgres?q=c%2B%2B%20and%20css%20difference&imgurl=https%3A%2F%2Fstatic.javatpoint.com%2Fcpp%2Fimages%2Fconstructor-vs-destructor-in-cpp.png&imgrefurl=https%3A%2F%2Fwww.javatpoint.com%2Fconstructor-vs-destructor-in-cpp&docid=CV1wKzMSVJQf8M&tbnid=xa7aUJT2-y9xJM&vet=12ahUKEwiog7Sz4rSHAxXyQEEAHeR_DDYQM3oECH8QAA..i&w=560&h=245&hcb=2&ved=2ahUKEwiog7Sz4rSHAxXyQEEAHeR_DDYQM3oECH8QAA',
  width: 400,
  height: 400
}
</script>
<!-- HTML -->
<template>
  <!-- <a v-bind:href="myChannel">HuXn Channel</a>
  <a :href="myChannel">HuXn Channel</a>
  <img :src="amazingImage" :width="imageWidth" :height="imageHeight" />  -->
  <!-- Dynamic Binding -->
  <img :src="imageInfo.src" />
  <h1>{{ myMessage }}</h1>
  <h2>{{ myNumber }}</h2>
  <h3>2 + 2 = {{ 2 + 2 }}</h3>
  <h1>Add two numbers {{ add(2, 2) }}</h1>
</template>

<!-- Css -->
<!-- <style></style> -->
