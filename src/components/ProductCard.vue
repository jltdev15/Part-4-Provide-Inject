<template>
    <div v-for="item in injectedData" :key="item.id" class="w-32 rounded">
        <header class="bg-green-500">
            <p>{{ item.name }}</p>
        </header>
        <p> Category :{{ item.category }}</p>
        <p>Quantity : {{ item.qty }}</p>
        <button @dblclick="doubleClickEvent" class="btn bg-blue-500 p-3 text-gray-50">Add To Cart</button>

    </div>
</template>

<script setup>
import { inject } from 'vue';

const injectedData = inject('products')
console.log(injectedData.value);
// const props = defineProps(['id', 'name', 'category', 'qty'])
const doubleClickEvent = () => {
    console.log('Double Click');
}

</script>