<script setup>
import { ref } from "vue";

const isLoaded = ref(false);
const isPlaying = ref(false);
const video = ref();

async function play() {
    await video.value.player.playVideo();
}
</script>


<template>
    <div class="py-8 md:lg:xl:py-24 md:lg:xl:px-64">
        <div class="flex-col justify-center md:lg:xl:py-12">
            <h1 class="text-3xl md:text-5xl lg:text-6xl font-bold text-center">See how easy it is for yourself…</h1>
            <p class="text-2xl md:text-4xl lg:text-5xl font-bold text-center">👀</p>
        </div>

        <div class="flex justify-center">
            <div
                class="flex items-center justify-center mx-auto px-8 md:lg:xl:p-1 h-48 md:lg:xl:h-[650px] md:lg:xl:w-[1100px]">
                <ScriptYouTubePlayer ref="video" style="width: 100%; height: 100%;"
                    class="rounded-2xl w-full max-w-3xl aspect-video overflow-hidden relative z-20"
                    label="about-application" video-id="d_IFKP1Ofq0" @ready="isLoaded = true"
                    @state-change="stateChange">
                    <template #awaitingLoad>
                        <div
                            class="absolute left-1/2 top-1/2 transform -translate-x-1/2 -translate-y-1/2 h-[48px] w-[68px]">
                            <svg height="100%" version="1.1" viewBox="0 0 68 48" width="100%">
                                <path
                                    d="M66.52,7.74c-0.78-2.93-2.49-5.41-5.42-6.19C55.79,.13,34,0,34,0S12.21,.13,6.9,1.55 C3.97,2.33,2.27,4.81,1.48,7.74C0.06,13.05,0,24,0,24s0.06,10.95,1.48,16.26c0.78,2.93,2.49,5.41,5.42,6.19 C12.21,47.87,34,48,34,48s21.79-0.13,27.1-1.55c2.93-0.78,4.64-3.26,5.42-6.19C67.94,34.95,68,24,68,24S67.94,13.05,66.52,7.74z"
                                    fill="#f00" />
                                <path d="M 45,24 27,14 27,34" fill="#fff" />
                            </svg>
                        </div>
                    </template>
                </ScriptYouTubePlayer>
            </div>
        </div>
    </div>
</template>