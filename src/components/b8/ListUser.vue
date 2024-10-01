<template>
  <div>
    <h2>List of Users</h2>

    <button @click="toggleForm">Add user</button>

    <FormAddUser :isVisible="showForm" @close="toggleForm" />
  </div>
</template>

<script setup>
import { ref } from 'vue'
import FormAddUser from './FormAddUser.vue'

const showForm = ref(false) 

const toggleForm = () => {
  showForm.value = !showForm.value 
}
</script>

<style>
</style>
