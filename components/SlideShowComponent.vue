<script setup lang="ts">
const images = ["/images/slideshow_img/slika1.jpg", "/images/slideshow_img/slika2.jpg", "/images/slideshow_img/slika3.jpg", "/images/slideshow_img/slika4.jpg", "/images/slideshow_img/slika5.jpg", "/images/slideshow_img/slika6.jpg"];
</script>

<template>
    <AppContainer class="flex flex-col text-center bg-orange-400 gap-6 pb-12">
        <AppSlideshow 
         :images
        />
    </AppContainer>
</template>