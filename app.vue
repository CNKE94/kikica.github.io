<script setup lang="ts">
useHead({
  htmlAttrs: {
    lang: "en",
  },
  link: [
    {
      rel: "icon",
      type: "image/x-icon",
      href: "/images/wedding-couple.svg",
    },
  ],
});

useSeoMeta({
  title: "Кристина & Иван",
  charset: "utf-8",
  viewport: "width=device-width, initial-scale=1",
  ogImage: {
    url: `/images/vencanje.jpg`,
    width: 1200,
    height: 630,
    type: "image/jpeg",
  },

})
</script>

<template>
  <div>
    <NuxtLayout>
      <NuxtPage />
    </NuxtLayout>
  </div>
</template>
