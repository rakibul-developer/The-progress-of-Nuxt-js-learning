<script setup>
const route = useRoute();
const slug = route.fullPath;
</script>

<template>
    <div>
        <h2>About Page - Dynamic Route</h2>
        <p>You are trying to access: <strong>{{ slug }}</strong></p>
        <NuxtLink to="/about">back to previous page</NuxtLink>
    </div>
</template>

