<template>
  <div>
    <h2>B1</h2>
    <ParentComponent></ParentComponent>

    <h2>B2</h2>
    <ProdctParent></ProdctParent>

    <h2>B3</h2>
    <CountParent></CountParent>

    <h2>B4</h2>
    <TodoApp></TodoApp>

    <h2>B5</h2>
    <div>
    <button @click="showModal = true">Open Modal</button>
    <Modal :isVisible="showModal" @close="showModal = false">
      <template #title>
        Thông báo từ hệ thống
      </template>
      <template #body>
        Đây là nội dung của modal. Bạn có thể đóng modal bằng cách nhấn vào nút 'Close'.
      </template>
    </Modal>
  </div>

    <h2>B6</h2>
    <div>
    <Card>
      <template #header>
        Thông tin sản phẩm
      </template>
      <template #body>
        Đây là mô tả ngắn gọn về sản phẩm này. Sản phẩm có các tính năng nổi bật và giá cả hợp lý.
      </template>
      <template #footer>
        <button @click="handleDetails">Xem chi tiết</button>
      </template>
    </Card>
  </div>
  <h2>B7</h2>
  <MessageParent></MessageParent>

  <h2>B8</h2>
  <ListUser></ListUser>
  </div>

    
</template>

<script setup>
import ParentComponent from "./components/b1/ParentComponent.vue"

import ProdctParent from "./components/b2/ProductParent.vue"

import CountParent from "./components/b3/CountParent.vue"
import TodoApp from "./components/b4/TodoApp.vue"

import { ref } from 'vue'
import Modal from './components/b5/Modal.vue'

const showModal = ref(false) 

import Card from './components/b6/Cart.vue'

const handleDetails = () => {
  alert('Xem chi tiết sản phẩm!');
}
  import MessageParent from "./components/b7/MessageParent.vue"
  import ListUser from './components/b8/ListUser.vue'
</script>

<style>

</style>