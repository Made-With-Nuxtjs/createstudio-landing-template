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
                        <a class="rounded-xs bg-emerald-500 h-5 w-5 flex justify-center items-center" href="/">
                            <Icon class="h-6 w-6" name="material-symbols-light:star-rate" style="color: white" />
                        </a>
                        <a class="rounded-xs bg-emerald-500 h-5 w-5 flex justify-center items-center" href="/">
                            <Icon class="h-6 w-6" name="material-symbols-light:star-rate" style="color: white" />
                        </a>
                        <a class="rounded-xs bg-emerald-500 h-5 w-5 flex justify-center items-center" href="/">
                            <Icon class="h-6 w-6" name="material-symbols-light:star-rate" style="color: white" />
                        </a>
                        <a class="rounded-xs bg-emerald-500 h-5 w-5 flex justify-center items-center ml-3" href="/">
                            <Icon class="h-6 w-6" name="material-symbols-light:star-rate" style="color: white" />
                        </a>
                    </div>
                    <div>
                        <p class="text-lg px-2 text-center"> <span class="font-bold">TrustPilot</span> <br
                                class="md:lg:xl:hidden" />
                            4.8. out
                            of 5 on 650+
                            reviews
                        </p>
                    </div>
                </div>
                <div class="flex justify-center p-2 md:p-8">
                    <h2
                        class="text-4xl md:text-3xl lg:text-5xl xl:text-6xl font-bold text-center  md:lg:xl:leading-loose px-8">
                        Easily Create 3D Animated <br class="hidden sm:block"> Videos in Just Minutes
                    </h2>
                </div>
                <div class="flex flex-wrap gap-1 md:lg:xl:gap-4 justify-center p-4">
                    <div class="flex gap-2 items-center">
                        <Icon class="h-8 w-8 font-bold rounded-full"
                            name="material-symbols-light:check-circle-outline-rounded" style="color: blue" />
                        <p class="text-lg font-bold text-gray-950/75">With ZERO Tech or Design Skills</p>
                    </div>
                    <div class="flex gap-2 items-center">
                        <Icon class="h-8 w-8 font-bold rounded-full"
                            name="material-symbols-light:check-circle-outline-rounded" style="color: blue" />
                        <p class="text-lg font-bold text-gray-950/75">Build Custom 3D Characters</p>
                    </div>
                    <div class="flex gap-2 items-center">
                        <Icon class="h-8 w-8 font-bold rounded-full"
                            name="material-symbols-light:check-circle-outline-rounded" style="color: blue" />
                        <p class="text-lg font-bold text-gray-950/75">#1 Rated Video Making Software</p>
                    </div>
                </div>
                <div class="relative">
                    <div
                        class="flex items-center justify-center mx-auto px-8 md:lg:xl:p-1 h-48 md:lg:xl:h-[500px] md:lg:xl:w-[900px]">
                        <ScriptYouTubePlayer ref="video" style="width: 100%; height: 100%;"
                            class="rounded-xl w-full max-w-3xl aspect-video overflow-hidden relative z-20"
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
                    <div class="flex justify-center">
                        <NuxtImg src="/img/left-avatar.avif" title="left-avatar" alt="image"
                            class="w-16 md:lg:xl:w-52 left-avatar-rotate absolute left-0 top-0" />
                        <NuxtImg src="/img/right-avatar.avif" title="right-avatar" alt="image"
                            class="w-56 hidden md:lg:xl:flex  absolute right-0 top-[-70px] right-avatar-rotate" />
                    </div>
                </div>
            </div>

            <!-- New Section -->
            <div class="relative overflow-auto">
                <!-- Background Container -->
                <div class="bg-indigo-600 blur-xs m-2 md:m-8 rounded-3xl py-8 relative">
                    <!-- Left Decorative Image -->
                    <NuxtImg src="/img/section1_outer_left.avif"
                        class="w-32 h-32 md:w-64 md:h-64 opacity-25 absolute top-16 left-0"
                        style="backdrop-filter: blur(50px);" title="bg-blur" alt="image" />

                    <!-- Main Content -->
                    <div class="flex flex-wrap justify-center gap-8 md:gap-16 items-center p-4">
                        <!-- Left Section: Product Image -->
                        <div class="flex justify-center basis-full md:basis-1/2 lg:basis-1/3">
                            <NuxtImg src="/img/section1.avif" class="w-[300px] md:w-[400px] lg:w-[600px] h-auto"
                                title="product" alt="image" />
                        </div>

                        <!-- Right Section: Text and Features -->
                        <div
                            class="basis-full md:basis-1/2 lg:basis-1/3 flex flex-col justify-center items-center text-center space-y-1 order-first md:lg:xl:order-last">
                            <p class="text-xl md:lg:xl:text-2xl text-gray-400 font-bold">
                                Limited-time lifetime deal <br />
                                Usually $197/year
                            </p>
                            <h1 class="text-5xl md:lg:xl:text-6xl text-gray-50 font-custom_3 uppercase">Today: ONLY $67!</h1>
                            <h2 class="text-4xl md:lg:xl:text-3xl text-gray-50 font-bold p-4">
                                (Pay Once, Use Forever)!
                            </h2>
                            <div class="flex justify-center">
                                <div
                                    class="p-4 cursor-pointer rounded-lg bg-[#ff1e1e] transition transform hover:-translate-y-1 hover:scale-110 hover:bg-red-500 duration-300">
                                    <p class="text-gray-50 text-xl md:lg:xl:text-2xl font-bold">Get CreateStudio Lifetime</p>
                                </div>
                            </div>
                            <h6 class="text-base md:text-xl text-gray-400 font-bold p-4">
                                Risk-Free 30 Day Money Back Guarantee
                            </h6>

                            <!-- Rating Section -->
                            <div class="flex flex-col justify-center items-center space-y-2">
                                <div class="flex space-x-1 justify-center">
                                    <a v-for="index in 4" :key="index"
                                        class="rounded-xs bg-teal-600 h-4 w-4 md:lg:xl:h-5 md:lg:xl:w-5 flex justify-center items-center"
                                        href="/">
                                        <Icon class="h-6 w-6" name="material-symbols-light:star-rate"
                                            style="color: white" />
                                    </a>
                                </div>
                                <p class="text-sm md:text-xl font-semibold text-gray-200">
                                    <span class="font-bold">TrustPilot</span> 4.8 out of 5 on 650+ reviews
                                </p>
                            </div>
                        </div>
                    </div>

                    <!-- Features Section -->
                    <div class="flex flex-wrap gap-4 justify-center py-8 px-4">
                        <div class="flex flex-col md:flex-row md:space-x-8 lg:space-x-16 gap-1 md:gap-4">
                            <div class="md:lg:xl:space-y-4">
                                <div class="flex gap-2 items-center">
                                    <Icon class="h-8 w-8 rounded-full"
                                        name="material-symbols-light:check-circle-outline-rounded"
                                        style="color: indigo" />
                                    <p class="text-lg md:lg:xl:text-xl font-bold text-gray-300">3D Character Creator</p>
                                </div>
                                <div class="flex gap-2 items-center">
                                    <Icon class="h-8 w-8 rounded-full"
                                        name="material-symbols-light:check-circle-outline-rounded"
                                        style="color: indigo" />
                                    <p class="text-lg md:lg:xl:text-xl font-bold text-gray-300">Unlimited Video Exports</p>
                                </div>
                            </div>

                            <div class="md:lg:xl:space-y-4">
                                <div class="flex gap-2 items-center">
                                    <Icon class="h-8 w-8 rounded-full"
                                        name="material-symbols-light:check-circle-outline-rounded"
                                        style="color: indigo" />
                                    <p class="text-lg md:lg:xl:text-xl font-bold text-gray-300">Automatic Lipsyncing</p>
                                </div>
                                <div class="flex gap-2 items-center">
                                    <Icon class="h-8 w-8 rounded-full"
                                        name="material-symbols-light:check-circle-outline-rounded"
                                        style="color: indigo" />
                                    <p class="text-lg md:lg:xl:text-xl font-bold text-gray-300">Doodle Video Creator</p>
                                </div>
                            </div>

                            <div class="md:lg:xl:space-y-4">
                                <div class="flex gap-2 items-center">
                                    <Icon class="h-8 w-8 rounded-full"
                                        name="material-symbols-light:check-circle-outline-rounded"
                                        style="color: indigo" />
                                    <p class="text-lg md:lg:xl:text-xl font-bold text-gray-300">Commercial Use License</p>
                                </div>
                                <div class="flex gap-2 items-center">
                                    <Icon class="h-8 w-8 rounded-full"
                                        name="material-symbols-light:check-circle-outline-rounded"
                                        style="color: indigo" />
                                    <p class="text-lg md:lg:xl:text-xl font-bold text-gray-300">Easy to use</p>
                                </div>
                            </div>

                            <div class="md:lg:xl:space-y-4">
                                <div class="flex gap-2 items-center">
                                    <Icon class="h-8 w-8 rounded-full"
                                        name="material-symbols-light:check-circle-outline-rounded"
                                        style="color: indigo" />
                                    <p class="text-lg md:lg:xl:text-xl font-bold text-gray-300">Drag & Drop Editor</p>
                                </div>
                                <div class="flex gap-2 items-center">
                                    <Icon class="h-8 w-8 rounded-full"
                                        name="material-symbols-light:check-circle-outline-rounded"
                                        style="color: indigo" />
                                    <p class="text-lg md:lg:xl:text-xl font-bold text-gray-300">Scroll Stopping Video Ads
                                    </p>
                                </div>
                            </div>
                        </div>
                    </div>

                    <!-- Right Decorative Image -->
                    <NuxtImg src="/img/section1_right.avif"
                        class="w-32 h-32 md:w-64 md:h-64 opacity-25 absolute top-16 right-0"
                        style="backdrop-filter: blur(5px);" title="bg-blur" alt="image" />
                </div>
            </div>


        </section>

        <!-- worldwide users section -->
        <section>
            <WorldwideUsers />
        </section>

        <!-- Analysis section -->
        <section>
            <Analysis />
        </section>

        <!-- Problem Identification section -->
        <section>
            <ProblemIdentification />
        </section>

        <!-- Introducing The Brand New section -->
        <section>
            <TheBrandNew />
        </section>
  <!-- See how easy it is for yourself section -->
        <section>
            <SeeHowEasy />
        </section>
        <!-- Simple Steps section -->
        <section>
            <SimpleSteps />
        </section>


    </main>
</template>