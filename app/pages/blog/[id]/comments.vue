<script setup>
const route = useRoute()
</script>

<template>
  <div>
    <h3>Comments for Post {{ route.params.id }}</h3>
  </div>
</template>
