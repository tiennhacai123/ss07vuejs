<template>
  <div v-if="isVisible" class="modal-overlay">
    <div class="modal">
      <div class="modal-header">
        <slot name="title"></slot>
      </div>
      <div class="modal-body">
        <slot name="body"></slot>   
      </div>
      <div class="modal-footer">
        <button @click="closeModal">Close</button>
      </div>
    </div>
  </div>
</template>

<script setup>
const props = defineProps({
  isVisible: {
    type: Boolean,
    required: true
  }
})

const emit = defineEmits(['close'])

const closeModal = () => {
  emit('close') 
}
</script>

<style>
.modal-overlay {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.5);
  display: flex;
  justify-content: center;
  align-items: center;
}

.modal {
  background: white;
  padding: 20px;
  border-radius: 5px;
  width: 300px;
  text-align: center;
}

.modal-header {
  font-weight: bold;
  margin-bottom: 10px;
}

.modal-body {
  margin-bottom: 20px;
}

.modal-footer button {
  background-color: #007bff;
  color: white;
  border: none;
  padding: 10px 20px;
  border-radius: 5px;
  cursor: pointer;
}

.modal-footer button:hover {
  background-color: #0056b3;
}
</style>
