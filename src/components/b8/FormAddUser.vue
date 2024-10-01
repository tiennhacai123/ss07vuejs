<template>
  <div v-if="isVisible" class="form-container">
    <form @submit.prevent="submitForm">
      <div>
        <label for="name">Name:</label>
        <input type="text" id="name" v-model="name" />
      </div>

      <div>
        <label for="email">Email:</label>
        <input type="email" id="email" v-model="email" />
      </div>

      <div>
        <label for="address">Address:</label>
        <input type="text" id="address" v-model="address" />
      </div>

      <button type="submit">Submit</button>
      <button type="button" @click="closeForm">Close</button>
    </form>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const props = defineProps({
  isVisible: Boolean
})

const emit = defineEmits(['close'])

const name = ref('')
const email = ref('')
const address = ref('')

const closeForm = () => {
  emit('close') 
}

const submitForm = () => {
  console.log({
    name: name.value,
    email: email.value,
    address: address.value
  })
  closeForm() 
}
</script>

<style>
.form-container {
  border: 1px solid #ccc;
  padding: 20px;
  background-color: #f9f9f9;
  width: 300px;
}
</style>
