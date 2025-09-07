<script lang="ts" setup>
const route = useRoute()

const LazyCardSection = defineAsyncComponent(() => import('~/components/Card.vue'))
</script>

<template>
  <div>
    <p>This is the blog post content for ID: {{ route.params.id }}</p>
    <client-only>
      <LazyCardSection />
    </client-only>
  </div>
</template>
