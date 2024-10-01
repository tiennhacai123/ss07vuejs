<template>
  <div>
    <h1>Parent Component</h1>
    <p>Current Count: {{ count }}</p>
    <CountChildren @increment="handleIncrement" />
  </div>
</template>

<script setup>
import { ref } from "vue";
import CountChildren from "./CountChildren.vue";

const count = ref(0);

const handleIncrement = () => {
  count.value++;
};
</script>

<style scoped>
h1 {
  color: blue;
}
</style>
