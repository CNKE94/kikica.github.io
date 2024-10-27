<script setup lang="ts">
const details = {
    title: 'КРИСТИНА & ИВАН',
    description: 'Вас позивају на своје венчање',
}
</script>

<template>
  <div class="relative lg:h-[100vh]">
    <NuxtImg
        class="object-cover w-full h-full"
        src="/images/vencanje.jpeg"
        alt="alt"
    />
    <div class="absolute top-1/3 lg:top-1/2 left-1/2 translate-x-[-50%] text-center w-full">
        <AppHeading class="text-6xl lg:text-8xl" heading="h1" :title="details.title" />
        <AppHeading class="text-3xl lg:text-5xl mt-5" heading="h2" :title="details.description" />
        <p class="w-3/4 mx-auto text-2xl lg:text-4xl mt-8 pt-8 lg:mt-14 lg:pt-14 border-t-4 border-orange-500">Субота, 31 Мај 2025</p>
    </div>
  </div>
</template>