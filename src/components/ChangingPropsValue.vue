<script setup>
const myFavouriteNumberProp = defineProps(['myFavouriteNumber'])
//myFavouriteNumberProp.myFavouriteNumber = 10
</script>

<template>
  <h1>{{ myFavouriteNumberProp.myFavouriteNumber }}</h1>
</template>
