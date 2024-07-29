<script setup>
import MeComponent from './MeComponent.vue'
import { onMounted, ref } from 'vue'

const myRef = ref(null)

onMounted(() => {
  console.log(myRef.value)
})
</script>

<template>
  <MeComponent ref="myRef" />
</template>
