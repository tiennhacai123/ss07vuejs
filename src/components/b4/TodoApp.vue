<template>
  <div>
    <h3>Todo List</h3>
    <ul>
      <li v-for="todo in todos" :key="todo.id">
        <TodoItem :todo="todo" @deleteTodo="deleteTodo" />
      </li>
    </ul>
  </div>
</template>

<script setup>
import { ref } from 'vue'
import TodoItem from './TodoItem.vue'

const todos = ref([
  { id: 1, text: 'Learn Vue.js' },
  { id: 2, text: 'Build a project' },
  { id: 3, text: 'Practice coding' }
])

const deleteTodo = (id) => {
  todos.value = todos.value.filter(todo => todo.id !== id)
}
</script>

<style>
</style>
