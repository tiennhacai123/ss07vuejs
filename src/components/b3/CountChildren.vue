<template>
  <div>
    <h2>Child Component</h2>
    <button @click="incrementCount">Increment</button>
  </div>
</template>

<script setup>
const incrementCount = () => {
  emit('increment')
}
const emit = defineEmits(['increment'])
</script>

<style scoped>
button {
  background-color: green;
  color: white;
  padding: 10px;
  border: none;
  cursor: pointer;
}

button:hover {
  background-color: darkgreen;
}
</style>
