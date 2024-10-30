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
        src="/images/vencanje.jpg"
        alt="alt"
    />
    <div class="flex flex-col h-full w-full justify-around absolute top-0 left-1/2 translate-x-[-50%] text-center px-4">
        <AppHeading
         class="text-4xl md:text-6xl lg:text-8xl" 
         heading="h1" 
         :title="details.title"
        />
        <div class="mt-20 lg:mt-0">
          <AppHeading 
           class="text-3xl md:text-4xl lg:text-5xl mt-5" 
           heading="h2" 
           :title="details.description"
          />
          <p class="w-3/4 mx-auto text-2xl lg:text-4xl mt-8 pt-8 lg:mt-14 lg:pt-14 border-t-4 border-orange-500">Субота, 31. мај 2025.</p>
        </div>
      </div>
  </div>
</template>