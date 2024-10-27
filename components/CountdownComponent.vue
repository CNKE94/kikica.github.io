<script setup lang="ts">

const targetDate = new Date(2025, 4, 31, 23, 59, 59);
const timeRemaining = ref({ days: 0, hours: 0, minutes: 0, seconds: 0 });
let intervalId: number | undefined;

const calculateTimeRemaining = () => {
  const now = new Date().getTime();
  const distance = targetDate.getTime() - now;

  if (distance <= 0) {
    clearInterval(intervalId);
    timeRemaining.value = { days: 0, hours: 0, minutes: 0, seconds: 0 };
  } else {
    const days = Math.floor(distance / (1000 * 60 * 60 * 24));
    const hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
    const minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
    const seconds = Math.floor((distance % (1000 * 60)) / 1000);
    timeRemaining.value = { days, hours, minutes, seconds };
  }
};

onMounted(() => {
  calculateTimeRemaining();
  intervalId = window.setInterval(calculateTimeRemaining, 1000);
});

onUnmounted(() => {
  if (intervalId) clearInterval(intervalId);
});
</script>

<template>
  <div class="py-8 text-center bg-orange-200">
    <AppHeading class="text-3xl lg:text-5xl mb-10" heading="h2" title="Венчање почиње за:" />
    <div class="flex justify-center gap-x-2 lg:gap-x-4">
        <AppCountdown :number="timeRemaining.days" subtitle="Дана" />
        <AppCountdown :number="timeRemaining.hours" subtitle="Сати" />
        <AppCountdown :number="timeRemaining.minutes" subtitle="Минута" />
        <AppCountdown :number="timeRemaining.seconds" subtitle="Секунди" />
    </div>
  </div>
</template>
