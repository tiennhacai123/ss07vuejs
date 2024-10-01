<template>
  <div>
    <h3>----------------Parent component----------------</h3>
    <p>Parent Company: {{ company }}</p>
    <ChildrenComponent :companyName="company"></ChildrenComponent>
  </div>
</template>

<script setup>
import ChildrenComponent from "./ChildrenComponent.vue";
import { ref } from "vue";
const company = ref("Rikkei Academy");
// console.log(company.value);
</script>

<style></style>
