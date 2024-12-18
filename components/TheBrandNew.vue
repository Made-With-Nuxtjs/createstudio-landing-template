<script>
const isLoaded = ref(false)
const isPlaying = ref(false)
const video = ref()
async function play() {
    await video.value.player.playVideo()
}

</script>

<template>
    <div class="bg-violet-950 pb-32 h-[1000px]">
        <div class="container mx-auto p-8">
            <h2 class="text-4xl text-gray-50 text-center font-custom_1">Introducing The Brand New </h2>
            <h1 class="text-6xl font-bold text-center text-gray-50 p-6 font-custom_2">CreateStudio 3.0 ✨</h1>
            <p class="text-center text-xl text-gray-50 px-64">The easiest 3D animation software for creators, business
                owners, and marketers to create every video they need to educate, explain & sell anything online!</p>
        </div>
        <div class="flex justify-center">
            <div
                class="bg-gradient-to-r from-[#FF416C] to-[#FF4B2B] rounded-xl text-white font-semibold px-4 cursor-pointer transition ease-in-out delay-150 bg-[#ff1e1e] hover:-translate-y-1 hover:scale-110 hover:bg-red-500 duration-300">
                <h3 class="text-xs md:lg:xl:text-2xl text-gray-50 text-center p-4">
                    Get My Lifetime Deal</h3>
            </div>
        </div>
        <div class="flex justify-center">
            <p class="text-lg text-gray-50 p-4">30 Day Money Back Guarantee</p>
        </div>
        <div class="flex-col justify-center gap-1 items-center">
            <div class="flex space-x-1 justify-center">
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
                <p class="text-lg font-semibold text-gray-200 px-2 text-center"> <span
                        class="font-bold">TrustPilot</span> 4.8. out of 5 on 650+ reviews
                </p>
            </div>
        </div>
        <div class="container mx-auto px-24 justify-center">
            <NuxtImg src="/img/brand_img.avif" alt="brand-image" title="brand-image" class="w-full" />

            <div class="py-12">
                <h1 class="text-6xl text-center font-bold ">See how easy it is for yourself… </h1>
                <p class="text-6xl text-center font-bold">👀</p>
            </div>

            <div class="flex justify-center">
                <div
                    class="flex items-center justify-center mx-auto px-8 md:lg:xl:p-1 h-48 md:lg:xl:h-[700px] md:lg:xl:w-[1200px]">
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
        .
    </div>
</template>