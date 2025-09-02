<script setup>
const route = useRoute()
</script>

<template>
  <div>
    <h1>User Profile for ID: {{ route.params.id }}</h1>
    <!-- <nav>
      <NuxtLink :to="`/users/${route.params.id}`">Profile</NuxtLink> |
      <NuxtLink :to="`/users/${route.params.id}/settings`">Settings</NuxtLink>
    </nav> -->

    <!-- এখানে child route render হবে -->
    <NuxtPage />
  </div>
</template>
