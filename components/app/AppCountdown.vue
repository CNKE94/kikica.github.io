<script setup lang="ts">
interface Props {
  number: number;
  subtitle: string;
}
defineProps<Props>();
</script>

<template>
    <div class="bg-slate-300 rounded-lg py-4 lg:py-8 px-1 min-w-20 lg:px-3 lg:min-w-44">
        <p class="text-2xl lg:text-5xl">{{ number }}</p>
        <p class="text-lg lg:text-3xl mt-2 lg:mt-5">{{ subtitle }}</p>
    </div>
</template>