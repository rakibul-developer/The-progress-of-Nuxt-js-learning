<script setup>
const router = useRouter();
console.log(router);

onMounted(() => {
    router.push('/blog');
})
</script>

<template>
  <div>
    <h2>Redirecting...</h2>
  </div>
</template>

