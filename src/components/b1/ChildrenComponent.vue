<template>
  <div>
    <h3>---------------ChildrenComponent---------------</h3>
    <p>Children Company: {{ props.companyName }}</p>
  </div>
</template>

<script setup>
const props = defineProps(["companyName"]);
</script>

<style></style>
