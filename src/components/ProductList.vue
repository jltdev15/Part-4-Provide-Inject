<template>
    <div class="grid grid-cols-3 items-center py-3 justify-center  w-5/6 mx-auto">
        <!-- <ProductCard v-for="item in props.product_data" :key="item.id" :name="item.name" :category="item.category"
            :qty="item.qty" /> -->
        <ProductCard />
    </div>
</template>

<script setup>

import ProductCard from './ProductCard.vue'

// const props = defineProps(['product_data'])


</script>