<script setup lang="ts">
interface Props {
  number: number;
  subtitle: string;
}
defineProps<Props>();
</script>

<template>
    <div class="bg-slate-300 rounded-lg p-3 min-w-44">
        <p class="text-5xl lg:text-7xl">{{ number }}</p>
        <p class="text-3xl lg:text-4xl mt-5">{{ subtitle }}</p>
    </div>
</template>