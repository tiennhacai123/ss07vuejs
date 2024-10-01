<template>
  <div>
    <h2>Du lieu trong component con</h2>
    <!-- không cần dùng props. cũng được -->
    <p>Id: {{productItem.Id}}</p> 
    <p>Product Name: {{productItem.ProductName}}</p>
    <p>Price: {{productItem.Price}}</p>
    <p>Quantity: {{productItem.Quantity}}</p>
  </div>
</template>

<script setup>
    const props = defineProps(["productItem"],)
    
</script>

<style></style>
