<script setup>
import { inject } from 'vue'
const friendsList = inject('friends')
const games = inject('games')
const moreGames = inject('moreGames')
</script>

<template>
  <h4>Injecting Array</h4>
  <ul v-for="(friend, index) in friendsList" :key="index">
    <li>{{ friend }}</li>
  </ul>
  <hr />
  <h4>Injecting Objects</h4>
  <ul v-for="(game, ind) in games" :key="ind">
    <li>{{ game }}</li>
  </ul>
  <hr />
  <h4>Injecting Array of Objects</h4>
  <ul v-for="(moreGame, i) in moreGames" :key="i">
    <li>{{ moreGame }}</li>
  </ul>
  <hr />
  <h4>Objects Destructuring</h4>
  <ul v-for="({ title, genre, platform, releaseDate }, index) in games" :key="index">
    <li>{{ title }}</li>
    <li>{{ genre }}</li>
    <li>{{ platform }}</li>
    <li>{{ releaseDate }}</li>
  </ul>
</template>
