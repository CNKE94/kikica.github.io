<script setup lang="ts">
const audio = ref<HTMLAudioElement | null>(null);

const playAudio = () => {
  if (audio.value) {
    audio.value.muted = true;
    audio.value.play().then(() => {
      audio.value!.muted = false;
    }).catch(error => {
      console.error("Error playing audio:", error);
    });
  }
};
</script>

<template>
  <div @scroll="playAudio">
    <MainComponent />
    <CountdownComponent />
    <EventSchedule />
    <FooterComponent />
    <SlideShowComponent />
    <AppSound />
  </div>
  <div>
    <audio
      ref="audio"
      src="/kristinaivanvencanje/sound/little-things.mp3"
    />
  </div>
</template>