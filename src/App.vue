<template>
  <div>
    <h1 class="p-12 text-3xl font-bold text-center bg-green-500 text text-gray-50">Demo Provide and Inject</h1>
    <ProductList :product_data="productList" />
  </div>
</template>

<script setup>
import { provide } from "vue";
import { ref } from "vue";
import ProductList from './components/ProductList.vue'



const productList = ref([
  {
    id: Date.now(),
    name: 'Samsung S4',
    category: 'Smart Phone',
    qty: 5,
  },
  {
    id: Date.now(),
    name: 'Iphone 15 Pro Max',
    category: 'Smart Phone',
    qty: 3,
  },
  {
    id: Date.now(),
    name: 'Xiaomi Mi 20',
    category: 'Smart Phone',
    qty: 5,
  }
])

// 2 arguments accept by provide function
provide('products', productList)
</script>