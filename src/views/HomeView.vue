<template>
  <div>
    <div v-if="isLoading">Loading...</div>
    <ul v-else>
      <li v-for="todo in data" :key="todo.id">{{ todo.title }}</li>
    </ul>
  </div>
</template>

<script setup lang="ts">
import { ref, onMounted } from 'vue'
import { useQuery, QueryClient } from '@tanstack/vue-query'
import axios from 'axios'

const queryClient = new QueryClient()

const { isLoading, data } = useQuery('todos', fetchData)

async function fetchData() {
  const response = await axios.get('http://localhost:3010')
  return response.data
}
</script>
