<script setup>
const route = useRoute()
</script>

<template>
  <div>
    <p>This is the settings page for user {{ route.params.id }}</p>
    <ul>
      <li><NuxtLink :to="`/users/${route.params.id}`">Back to Profile</NuxtLink></li>
      <li><NuxtLink to="/">home</NuxtLink></li>
    </ul>
  </div>
</template>
