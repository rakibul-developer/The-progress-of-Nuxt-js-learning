<script setup>
const route = useRoute()
</script>

<template>
  <div>
    <h2>Blog Post ID: {{ route.params.id }}</h2>
    <nav>
      <NuxtLink :to="`/blog/${route.params.id}`">Post</NuxtLink> |
      <NuxtLink :to="`/blog/${route.params.id}/comments`">Comments</NuxtLink> |
      <NuxtLink to="/">Home</NuxtLink>
    </nav>

    <!-- এখানে child route গুলো render হবে -->
    <NuxtPage />
  </div>
</template>
