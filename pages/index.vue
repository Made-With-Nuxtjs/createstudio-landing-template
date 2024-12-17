<script setup lang="ts">
useSeoMeta({
    title: 'CreateStudio Special Deal',
})

const isLoaded = ref(false)
const isPlaying = ref(false)
const video = ref()
async function play() {
    await video.value.player.playVideo()
}
function stateChange(event: { data: number; }) {
    isPlaying.value = event.data === 1
}


</script>

<template>
    <main>
        <!-- Hero Section -->
        <section>
            <div class="container mx-auto">
                <div class="flex md:lg:xl:flex-row flex-col justify-center gap-1 items-center">
                    <div class="flex space-x-1">
                        <a class="rounded-xs bg-teal-600 h-5 w-5 flex justify-center items-center" href="/">
                            <Icon class="h-6 w-6" name="material-symbols-light:star-rate" style="color: white" />
                        </a>
                        <a class="rounded-xs bg-teal-600 h-5 w-5 flex justify-center items-center" href="/">
                            <Icon class="h-6 w-6" name="material-symbols-light:star-rate" style="color: white" />
                        </a>
                        <a class="rounded-xs bg-teal-600 h-5 w-5 flex justify-center items-center" href="/">
                            <Icon class="h-6 w-6" name="material-symbols-light:star-rate" style="color: white" />
                        </a>
                        <a class="rounded-xs bg-teal-600 h-5 w-5 flex justify-center items-center" href="/">
                            <Icon class="h-6 w-6" name="material-symbols-light:star-rate" style="color: white" />
                        </a>
                    </div>
                    <div>
                        <p class="text-xl font-semibold px-2 text-center"> <span class="font-bold">TrustPilot</span> 4.8. out
                            of 5 on 650+
                            reviews
                        </p>
                    </div>
                </div>
                <div class="flex justify-center p-2 md:p-8">
                    <h2
                        class="text-2xl md:text-3xl lg:text-5xl xl:text-6xl font-bold text-center leading-relaxed md:leading-loose">
                        Easily Create 3D Animated <br class="hidden sm:block"> Videos in Just Minutes
                    </h2>
                </div>
                <div class="flex flex-wrap gap-1 md:lg:xl:gap-4 justify-center p-4">
                    <div class="flex gap-2 items-center">
                        <Icon class="h-8 w-8 font-bold rounded-full" name="material-symbols-light:check-circle-outline-rounded"
                            style="color: blue" />
                        <p class="text-lg font-bold">With ZERO Tech or Design Skills</p>
                    </div>
                    <div class="flex gap-2 items-center">
                        <Icon class="h-8 w-8 font-bold rounded-full" name="material-symbols-light:check-circle-outline-rounded"
                            style="color: blue" />
                        <p class="text-lg font-bold">Build Custom 3D Characters</p>
                    </div>
                    <div class="flex gap-2 items-center">
                        <Icon class="h-8 w-8 font-bold rounded-full" name="material-symbols-light:check-circle-outline-rounded"
                            style="color: blue" />
                        <p class="text-lg font-bold">#1 Rated Video Making Software</p>
                    </div>
                </div>
                <div class="relative">
                    <div class="flex items-center justify-center mx-auto px-8 md:lg:xl:p-1 h-48 md:lg:xl:h-[500px] md:lg:xl:w-[950px]">
                        <ScriptYouTubePlayer ref="video" style="width: 100%; height: 100%;"
                            class="rounded-xl w-full max-w-3xl aspect-video overflow-hidden relative z-20" label="about-application" video-id="d_IFKP1Ofq0" @ready="isLoaded = true"
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
                    <div class="flex justify-center">
                        <NuxtImg src="/img/left-avatar.avif" title="left-avatar" alt="image" class="w-16 md:lg:xl:w-52 left-avatar-rotate absolute left-0 top-0" />
                        <NuxtImg src="/img/right-avatar.avif" title="right-avatar" alt="image" class="w-56 hidden md:lg:xl:flex  absolute right-0 top-[-70px] right-avatar-rotate" />
                    </div>
                </div>
        
            </div>
            <div class="relative overflow-auto">
                <NuxtImg src="/img/section1_outer_left.avif" class="w-8 h-8" title="bg-blur" alt="image" />
                <div class="flex h-96 bg-indigo-500 m-2 md:lg:xl:m-8 rounded-3xl">
        
                </div>
            </div>
        </section>

        <!-- worldwide users section -->
         <section>
            <WorldwideUsers/>
         </section>

          <!-- worldwide users section -->
          <section>
            <div class="h-96">
                
            </div>
         </section>


    </main>
</template>