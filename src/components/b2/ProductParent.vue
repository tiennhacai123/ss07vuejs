<template>
    <div>
        <ProductChildren :productItem="product"></ProductChildren>
    </div>
</template>

<script setup>
    import ProductChildren from './ProductChildren.vue'
    import { reactive} from 'vue'
    const product = reactive({
        Id:1,
        ProductName : "Qua khe",
        Price: "99 999$",
        Quantity: 10
    })
    // console.log(product.ProductName);
    
</script>
    
<style>

</style>