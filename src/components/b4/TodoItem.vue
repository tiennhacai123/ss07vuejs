<template>
  <div>
    <span>{{ todo.text }}</span>
    <button @click="handleDelete">Delete</button>
  </div>
</template>

<script setup>
const props = defineProps({
  todo: {
    type: Object,
    required: true,
  },
});

const emit = defineEmits(["deleteTodo"]);

const handleDelete = () => {
  emit("deleteTodo", props.todo.id);
};
</script>

<style></style>
