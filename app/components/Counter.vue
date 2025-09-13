<template>
  <div>
    <h2>Counter Component</h2>
    <p>Count: {{counterStore.count}}</p>
    <p>Double Count: {{counterStore.doubleCount}}</p>
    <button @click="counterStore.increment()">Increment</button>
    <button @click="counterStore.decrement()">Decrement</button>
    <button @click="counterStore.reset()">Reset</button>
  </div>
</template>

<script lang="ts" setup>
import { useCounterStore } from '@/stores/counter'

const counterStore = useCounterStore()
</script>

<style>

</style>