<template>
  <div>
    <button @click="sendMessage">Send message</button>
  </div>
</template>

<script setup>
const emit = defineEmits(['messageSent'])

const sendMessage = () => {
  emit('messageSent') 
}
</script>

<style>

</style>
