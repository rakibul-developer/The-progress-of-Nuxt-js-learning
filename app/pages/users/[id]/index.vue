<script setup>
const route = useRoute()
</script>

<template>
  <div>
    <p>This is the profile content for user {{ route.params.id }}</p>
    <ul>
      <li><NuxtLink :to="`/users/${route.params.id}/settings`">Go to Settings</NuxtLink></li>
      <li><NuxtLink to="/">home</NuxtLink></li>
    </ul>
  </div>
</template>
