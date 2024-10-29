<script setup lang="ts">
const audio = ref<HTMLAudioElement | null>(null);

const playAudio = () => {
    if (audio.value) {
        audio.value.play()
        .then(() => {
                if (audio.value) {
                    audio.value.muted = false;
                }
            })
        .catch(error => {
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