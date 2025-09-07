<template>
    <div>
        <h3>Product List Page</h3>
        <input v-model="newProduct" type="text" placeholder="Add Your New Product" />
        <button
            :disabled="newProduct.trim() === ''"
            @click="addProduct"
        >
            Add Product
        </button>
        <p v-if="!products.length">No product found!</p>
        <ul style="list-style-type: none;" v-else>
            <li v-for="(product, index) in products"
            :key="index">
                <p>{{ index + 1 }}. {{ product }}</p>
            </li>
        </ul>
        <br>
        <NuxtLink to="/">Back to Home</NuxtLink>
    </div>
</template>

<script lang="ts" setup>
import { ref } from 'vue';

const newProduct = ref('');
const products = ref<string[]>([]);

const addProduct = () => {
    if (newProduct.value.trim() !== '') {
        products.value.push(newProduct.value);
        newProduct.value = '';
    }
}
</script>

