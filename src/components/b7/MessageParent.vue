<template>
  <div>
    <h3>Message Parent</h3>
    <MessageChildren @messageSent="handleMessage"></MessageChildren>
    <p v-if="message">{{ message }}</p>
  </div>
</template>

<script setup>
import { ref } from 'vue'
import MessageChildren from './MessageChildren.vue'

const message = ref('')

const handleMessage = () => {
  message.value = 'You have received a message from the child component!' 
}
</script>

<style>
</style>
