<script setup>
const route = useRoute()
</script>

<template>
  <div>
    <p>This is the blog post content for ID: {{ route.params.id }}</p>
  </div>
</template>
