<template>
  <div>
    <NuxtPage />
  </div>
</template>

<script setup>
const router = useRouter()
const currentPath = computed(
  () => `https://mitori.me${router.currentRoute.value.path}`
)

useHead({
  meta: [{
    property: 'og:url', content: currentPath
  }]
})
</script>
