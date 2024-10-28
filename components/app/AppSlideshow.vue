<script setup lang="ts">
import { ref, onMounted, onBeforeUnmount } from "vue";

interface SlideProps {
  images: string[];
  slideDuration?: number;
  transitionDuration?: number;
}

const props = defineProps<SlideProps>();

const slideDuration = props.slideDuration || 3000;
const transitionDuration = props.transitionDuration || 500;

const currentIndex = ref(0);
const intervalId = ref<ReturnType<typeof setInterval> | null>(null);

const nextSlide = () => {
  currentIndex.value = (currentIndex.value + 1) % props.images.length;
};

const startSlideshow = () => {
  intervalId.value = setInterval(nextSlide, slideDuration);
};

const pauseSlideshow = () => {
  if (intervalId.value) clearInterval(intervalId.value);
};

onMounted(startSlideshow);
onBeforeUnmount(pauseSlideshow);
</script>

<template>
  <div class="mx-auto rounded-md overflow-hidden relative lg:w-2/3">
    <div
      class="flex transition-transform ease-in-out duration-[2000ms]"
      :style="{ transform: `translateX(-${currentIndex * 100}%)` }"
    >
      <NuxtImg
          v-for="(image, index) in props.images"
          :key="index"
          :src="image"
          class="flex-shrink-0 w-full h-80 sm:h-[500px] md:h-[400px] lg:h-[550px] bg-cover bg-center object-cover"
        />
    </div>
  </div>
</template>
