<script setup lang="ts">
interface Props {
  heading: string;
  title: string;
  style?: string;
}
defineProps<Props>();
</script>

<template>
    <component :class="style" :is="heading">
        {{ title }}
    </component>
</template>