<script setup lang="ts">
const audio = ref<HTMLAudioElement | null>(null);

const playAudio = () => {
    if (audio.value) {
        audio.value.muted = true; // Start muted to bypass autoplay restrictions
        audio.value.play().then(() => {
            audio.value!.muted = false; // Unmute once playback begins
        }).catch(error => {
            console.error("Error playing audio:", error);
        });
    }
};

onMounted(() => {
    playAudio();
});
</script>

<template>
    <div>
        <audio
            ref="audio"
            src="/kikica.github.io/sound/little-things.mp3"
        />
    </div>
</template>