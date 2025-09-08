<template>
  <div>
    <h3>Cart Page</h3>
    <input 
      v-model="newCartName"
      type="text"
      placeholder="Add New Cart Item"
    >
    <p>{{ newCartName }}</p>

    <button
      :disabled="newCartName.trim() === '' || cart.items.length >= 3"
      @click="addToCart"
    >
      Add to Cart
    </button>

    <p>Total Cart: {{ cart.items.length }}</p>
    <p>Total: {{ cart.total }}</p>

    <p v-if="!cart.items.length">No cart item found!</p>

    <ul style="list-style-type: none;" v-else>
      <li style="display: flex; gap: 10px; align-items: center;"
          v-for="(item, index) in cart.items"
          :key="index"
      >
        <span>{{ index + 1 }}.</span>
        <p>{{ item }}</p>
      </li>
    </ul>

    <p v-if="maximumCart">You have reached the maximum limit of 3 items in the cart.</p>
  </div>
</template>

<script lang="ts" setup>
  import { ref, reactive, computed, watch } from 'vue';

  const newCartName = ref('');
  const cart = reactive<{
    items: string[];
    total: number; 
  }>({
      items: [],
      total: 0,
    });
  
  const maximumCart = computed(() => cart.items.length >= 3);

  watch(newCartName, (newValue, oldValue) => {
    console.log('Cart Name changed from', oldValue, 'to', newValue);
  });

  const addToCart = () => {
    if (cart.items.length !== 3) {
      cart.items.push(newCartName.value);
      newCartName.value = '';
      cart.total += 10;      
    }
  }
</script>