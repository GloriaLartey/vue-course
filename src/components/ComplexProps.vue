<script setup>
defineProps({
  friends: Array,
  userInfo: Object
})
</script>

<template>
  <h1>{{ friends }}</h1>
  <h1>{{ userInfo }}</h1>
  <hr />
  <!-- Iterating Over Friends Array -->
  <ul v-for="(friend, index) in friends" :key="index">
    <li>{{ friend }}</li>
  </ul>

  <!-- Object  -->
  <ul v-for="(info, i) in userInfo" :key="i">
    <li>{{ info }}</li>
  </ul>
</template>
