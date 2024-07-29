<script setup>
import { ref } from 'vue'

const newTask = ref('')
const tasks = ref([])

const addTask = () => {
  if (newTask.value.trim() != '') {
    tasks.value.push(newTask.value)
    newTask.value = ''
  }
}

const removeTask = (index) => {
  tasks.value.splice(index, 1)
}
</script>

<template>
  <div class="todo-ap">
    <div class="task-input">
      <input v-model="newTask" @keyup.enter="addTask" placeholder="Add new Todo" />
      <button @click="addTask">Add To Do</button>
    </div>

    <!-- Rendering all the tasks -->

    <ul class="task-list">
      <li v-for="(task, index) in tasks" :key="index" class="task-item">
        {{ task }}
      </li>
      <button @click="removeTask(index)" class="remove-button">Remove</button>
    </ul>
  </div>
</template>
