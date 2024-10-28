<script setup lang="ts">
import { useRuntimeConfig } from "#imports";
const runtimeConfig = useRuntimeConfig();

useHead({
  htmlAttrs: {
    lang: "en",
  },
  link: [
    {
      rel: "icon",
      type: "image/x-icon",
      href: "/kikica.github.io/images/wedding-couple.svg",
    },
  ],
});

useSeoMeta({
  title: "Кристина & Иван",
  charset: "utf-8",
  viewport: "width=device-width, initial-scale=1",
  ogImage: {
    url: `https://cnke94.github.io/kikica.github.io/images/vencanje.jpg`,
    width: 1200,
    height: 630,
    type: "image/jpeg",
  },
});
</script>

<template>
  <div>
    <NuxtLayout>
      <NuxtPage />
    </NuxtLayout>
  </div>
</template>
