<template>
    <div class="bg-black">
        <div class="container mx-auto px-6 md:px-16 py-16">
            <div class="flex flex-col md:flex-row justify-between">
                <!-- Left Section -->
                <div class="mb-8 md:mb-0 md:lg:xl:basis-1/4">
                    <div class="flex items-center mb-4">
                        <NuxtImg src="https://placehold.co/150x48" title="company-logo" alt="logo-image"
                            class="w-[160px] h-[50px]" />
                    </div>
                    <p class="mb-4 text-gray-300/75 text-xl font-semibold">
                        The absolute easiest tool ever for making unbelievably awesome professional animated explainer
                        videos, with click and drag ease of use.
                    </p>
                    <p class="my-4 pt-8 text-gray-300/75 text-xl font-semibold">
                        CreateStudio a software product of Vidello Limited. All rights reserved.
                    </p>
                </div>

                <!-- Links Section -->
                <div
                    class="flex flex-col md:flex-row space-y-8 md:space-y-0 md:space-x-16 text-gray-200/50  md:lg:xl:basis-1/2">
                    <div>
                        <div class="flex justify-between">
                            <h3 class="text-2xl font-bold mb-4">Resources</h3>
                            <Icon @click="openResource" class="h-10 w-10 md:lg:xl:hidden" :name="resources_arrow ? 'material-symbols-light:keyboard-arrow-up' : 'material-symbols-light:keyboard-arrow-down'"
                                style="color: white" />
                        </div>
                        <ul :class="resources_arrow ? 'space-y-3 text-xl' : 'space-y-3 text-xl hidden md:lg:xl:inline' ">
                            <li class="text-gray-800/75 hover:text-gray-300/75"><a href="/">CreateStudio Blog</a></li>
                            <li class="text-gray-800/75 hover:text-gray-300/75"><a href="/">CreateStudio FB Group</a>
                            </li>
                            <li class="text-gray-800/75 hover:text-gray-300/75"><a href="/">YouTube Channel</a></li>
                        </ul>
                    </div>
                    <div>
                        <div class="flex justify-between">
                            <h3 class="text-2xl font-bold mb-4">Support</h3>
                            <Icon @click="openSupport" class="h-10 w-10 md:lg:xl:hidden" :name="support_arrow ? 'material-symbols-light:keyboard-arrow-up' : 'material-symbols-light:keyboard-arrow-down'"
                                style="color: white" />
                        </div>
                        <ul :class="support_arrow ? 'space-y-3 text-xl' : 'space-y-3 text-xl hidden md:lg:xl:inline' ">
                            <li class="text-gray-800/75 hover:text-gray-300/75"><a href="/">Knowledgebase</a></li>
                            <li class="text-gray-800/75 hover:text-gray-300/75"><a href="/">Support Desk</a></li>
                            <li class="text-gray-800/75 hover:text-gray-300/75"><a href="/">Tutorials</a></li>
                            <li class="text-gray-800/75 hover:text-gray-300/75"><a href="/">Contact Us</a></li>
                        </ul>
                    </div>
                    <div>
                        <div class="flex justify-between">
                            <h3 class="text-2xl font-bold mb-4">Legal</h3>
                            <Icon @click="openLegal" class="h-10 w-10 md:lg:xl:hidden" :name="legal_arrow ? 'material-symbols-light:keyboard-arrow-up' : 'material-symbols-light:keyboard-arrow-down'"
                                style="color: white" />
                        </div>
                        <ul :class="legal_arrow ? 'space-y-3 text-xl' : 'space-y-3 text-xl hidden md:lg:xl:inline' ">
                            <li class="text-gray-800/75 hover:text-gray-300/75"><a href="/">Privacy Policy</a></li>
                            <li class="text-gray-800/75 hover:text-gray-300/75"><a href="/">Terms of Use</a></li>
                            <li class="text-gray-800/75 hover:text-gray-300/75"><a href="/">Disclaimer</a></li>
                            <li class="text-gray-800/75 hover:text-gray-300/75"><a href="/">Cookie Policy</a></li>
                        </ul>
                    </div>
                </div>
            </div>

            <!-- Disclaimer Section -->
            <div class="mt-8 text-sm text-gray-300/75">
                <p class="mb-4 text-lg">
                    This site is not a part of the Facebook website or Facebook INC. Additionally, this site is NOT
                    endorsed by Facebook in ANY WAY. Facebook is a trademark of Facebook INC. You understand this to be
                    an expression of opinions and not professional advice. You are solely responsible for the use of any
                    content and hold Vidello LLC and all members and affiliates harmless in any event or claim. You can
                    also safely assume that I get paid anytime you click on a link on this site. We recommend that you
                    do
                    your own Independent research before purchasing anything.
                </p>
                <p class="text-lg">
                    Disclaimer: We do NOT believe in get rich quick programs. We believe in hard work, adding value and
                    dedication to reach your goals. It’s a fact that one that does not take action will see no results
                    whatsoever. The results featured on this page are not the norm and are extraordinary results from
                    hard work, commitment and dedication by following through and taking action. You will get no results
                    whatsoever if you assume by soaking up information products, joining program after program your life
                    will change with riches. This is not for you. Your results are based upon your actions. If you want
                    a magic button that will fulfil your life with riches then please leave this page and do NOT
                    purchase. Our products are intended to help you share your message with the world whilst growing
                    your business. We don’t make any guarantees about your own results because we don’t know you.
                    Results in life are solely based on decisions made. We are here to help and guide you to move
                    forward faster by giving you awesome content, direction and strategies to reach your end goal.
                    Please check the content thoroughly on this page and that you are committed to taking relentless
                    action and will put in the effort before you decide to make a purchase. If not then please leave
                    this page and do not purchase.
                </p>
            </div>
        </div>
    </div>
</template>

<script setup lang="ts">
const resources_arrow = ref(false)
const support_arrow = ref(false)
const legal_arrow = ref(false)

 function openResource(){
    resources_arrow.value = !resources_arrow.value
 }

 function openSupport(){
    support_arrow.value = !support_arrow.value
 }
 
 function openLegal(){
    legal_arrow.value = !legal_arrow.value
 }
</script>