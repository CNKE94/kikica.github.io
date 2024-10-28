<script setup lang="ts">
interface Props {
  heading: string;
  icon?: string;
  time: string;
  place: string;
  address: string;
  style?: string;
}
defineProps<Props>();
</script>

<template>
    <div class="flex flex-col px-10 pt-10 pb-4 bg-white rounded-lg text-center gap-y-4">
        <AppHeading class="text-3xl font-bold" heading="h2" :title="heading" />
        <NuxtImg :src="icon" alt="icon" class="w-20 mx-auto" />
        <p>{{ time }}</p>
        <p>{{ place }}</p>
        <p>{{ address }}</p>
    </div>
</template>