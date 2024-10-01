<template>
  <div class="card">
    <div class="card-header">
      <slot name="header"></slot>
    </div>

    <div class="card-body">
      <slot name="body"></slot>
    </div>

    <div class="card-footer">
      <slot name="footer"></slot>
    </div>
  </div>
</template>

<script setup></script>

<style>
.card {
  border: 1px solid #ccc;
  border-radius: 5px;
  padding: 10px;
  margin: 20px;
  width: 300px;
}

.card-header,
.card-footer {
  background-color: #f7f7f7;
  padding: 10px;
  font-weight: bold;
}

.card-body {
  padding: 10px;
}

.card-footer {
  text-align: right;
}
</style>
