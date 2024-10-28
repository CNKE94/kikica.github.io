<script setup lang="ts">
const images = ["/images/vencanje.jpeg", "/images/vencanje.jpeg", "/images/vencanje.jpeg"];
</script>

<template>
    <AppContainer class="flex flex-col text-center bg-orange-400 gap-6">
        <AppSlideshow 
         :images
         :transition-duration="5000"
        />
    </AppContainer>
</template>