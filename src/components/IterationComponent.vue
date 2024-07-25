<script setup>
import { ref } from 'vue'
let people = ref(['Alex', 'Jordan', 'Ria'])

const books = ref([
  {
    id: 1,
    title: 'To Kill a Mockingbird',
    author: 'Harper Lee',
    genre: 'Fiction',
    publicationYear: 1960
  },
  { id: 2, title: '1984', author: 'George Orwell', genre: 'Dystopian', publicationYear: 1949 },
  {
    id: 3,
    title: 'The Great Gatsby',
    author: 'F. Scott Fitzgerald',
    genre: 'Classic',
    publicationYear: 1925
  },
  {
    id: 4,
    title: 'The Catcher in the Rye',
    author: 'J.D. Salinger',
    genre: 'Coming-of-age',
    publicationYear: 1951
  },
  {
    id: 5,
    title: "Harry Potter and the Soccerer's Stone",
    author: 'J.K. Rowling',
    genre: 'Fantasy',
    publicationYear: 1997
  }
])

const formData = ref({ username: '', email: '', Password: '' })
</script>

<template>
  <p v-for="(person, index) in people" :key="index">{{ person }}</p>

  <ul v-for="(id, title, author, genre, publicationYear, i) in books" :key="i">
    <li>ID: {{ id }}</li>
    <li>Title: {{ title }}</li>
    <li>Author: {{ author }}</li>
    <li>Genre: {{ genre }}</li>
    <li>Publication Year: {{ publicationYear }}</li>
  </ul>

  <form @submit.prevent="alert('Form Submitted')">
    <input type="text" placeholder="Please enter your name" v-model="formData.username" />
    <input type="email" placeholder="Please enter your email" v-model="formData.email" />
    <input type="password" placeholder="Please enter your password" v-model="formData.Password" />
    <button type="submit">Submit</button>
  </form>
  <h1>{{ formData.username }}</h1>
  <h1>{{ formData.email }}</h1>
  <h1>{{ formData.Password }}</h1>
</template>
