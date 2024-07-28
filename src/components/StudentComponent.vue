<script setup>
// defineProps(['studentName', 'studentAge', 'studentLocation'])

import { inject } from 'vue'

const studentName2 = inject('studentName2')
const studentAge2 = inject('studentAge2')
const studentLocation2 = inject('studentLocation2')
</script>

<template>
  <!-- <h1>Student Component (child)</h1>
  <h1>{{ studentName }}</h1>
  <h1>{{ studentAge }}</h1>
  <h1>{{ studentLocation }}</h1> -->

  <h1>Student Component (child)</h1>
  <h1>{{ studentName2 }}</h1>
  <h1>{{ studentAge2 }}</h1>
  <h1>{{ studentLocation2 }}</h1>
</template>
