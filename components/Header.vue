<template>
    <!-- Top Section -->
    <div class="bg-violet-600 sticky top-0 z-30">
        <div class="flex flex-col md:lg:xl:flex-row gap-2 md:lg:xl:gap-8 px-2 pt-1 md:lg:xl:pt-0 justify-center">
            <div>
                <h4 class="text-gray-50 p-1 text-center text-lg font-semibold"><span class="font-bold">New CreateStudio
                        3.0 Lifetime Deal:</span> Lifetime
                    special for a
                    limited-time only</h4>
            </div>
            <div
                class="p-1 flex justify-center items-center transition ease-in-out delay-300 hover:-translate-y-1 hover:scale-110 duration-300">
                <Icon name="material-symbols-light:arrow-right-alt" style="color: white" size="lg" class="h-6 w-6" />
                <p class="text-gray-50 font-bold text-lg">Get offer now</p>
            </div>
        </div>
    </div>


    <!-- Navigation -->
    <div class="container mx-auto p-4">
        <div class="flex justify-between items-center">
            <!-- Logo -->
            <div class="relative">
                <NuxtImg src="https://placehold.co/128x32" title="company-logo" alt="logo-image"
                    class="w-[160px] h-[50px]" />
                <span
                    class="absolute top-[-3px] right-0 bg-blue-500 text-white text-xs font-semibold px-2 rounded-full">
                    Pro
                </span>
            </div>

            <!-- Desktop Menu -->
            <div class="hidden md:flex gap-4 items-center">
                <button class="hover:bg-gray-200 px-2 py-1 rounded-lg text-gray-950 font-bold">Learn</button>
                <button
                    class="flex justify-center items-center hover:bg-gray-200 pl-2 py-1 rounded-lg text-gray-950 font-bold">Support
                    <Icon v-if="!isMenuOpen" name="material-symbols-light:keyboard-arrow-down" style="color: black"
                        class="h-6 w-6" />
                </button>
                <button
                    class="text-gray-50 rounded-lg font-bold transition bg-sky-500 hover:-translate-y-1 hover:scale-110 hover:bg-sky-400 duration-300 px-4 py-1">
                    Buy now
                </button>
            </div>

            <!-- Mobile Menu Button -->
            <div class="md:hidden">
                <button @click="toggleMenu" class="text-gray-950 focus:outline-none">
                    <!-- Menu Icon -->
                    <Icon v-if="!isMenuOpen" name="material-symbols-light:menu-rounded" style="color: black"
                        class="h-10 w-10" />
                    <!-- Close Icon -->
                    <Icon v-else name="material-symbols-light:close-rounded" style="color: black" class="h-10 w-10" />
                </button>
            </div>
        </div>

        <!-- Mobile Menu -->
        <div v-if="isMenuOpen" class="md:hidden bg-white w-full transition-transform duration-500 shadow-sm">
            <div class="p-2 space-y-2">
                <button class="block px-4 py-1 font-bold rounded-lg text-gray-700 bg-gray-200">Learn</button>
                <a href="#" class="flex items-center gap-2 px-4 py-1 font-bold rounded-lg text-gray-700 bg-gray-200">Support
                    <Icon name="material-symbols-light:keyboard-arrow-up" style="color: black" class="h-6 w-6" />

                </a>
                <ul class="p-4 space-y-6">
                    <li><a href="/" class="flex items-center font-bold gap-2">
                            <Icon name="material-symbols-light:library-books-outline-sharp" style="color: black"
                                class="h-8 w-8" />
                            KnowledgeBase
                        </a></li>
                        <li><a href="/" class="flex items-center font-bold gap-2">
                            <Icon name="material-symbols-light:mail-outline" style="color: black"
                                class="h-8 w-8" />
                                Support Desk
                        </a></li>
                        <li><a href="/" class="flex items-center font-bold gap-2">
                            <Icon name="material-symbols-light:chat-outline-sharp" style="color: black"
                                class="h-8 w-8" />
                                Live Chat
                        </a></li>
                </ul>
                <div class="pt-8 pb-4">
                    <a href="#"
                        class="px-4 py-1 text-center rounded-lg bg-sky-500 text-white font-bold hover:bg-sky-400">
                        Buy now
                    </a>
                </div>
            </div>
        </div>
    </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';

// State to track menu open/close status
const isMenuOpen = ref(false);

// Toggle function
function toggleMenu() {
    isMenuOpen.value = !isMenuOpen.value;
}
</script>