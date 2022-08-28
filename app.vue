<template>
  <NuxtLayout>
    <NuxtPage />
  </NuxtLayout>
</template>

<script setup>
useHead({
  viewPort: "width=device-width, initial-scale=1, maximum-scale=1",
  charset: "utf-8",
  link: [{ rel: "icon", type: "image/x-icon", href: "/favicon.ico" }]
})
</script>