<template>
    <SectionBase 
        class="pt-[12rem] -mt-[5.25rem]"
        crosses
        crossesOffset="lg:translate-y-[5.25rem]"
        customPaddings
        id="hero"
    >
        <div class="container relative" ref="container">
            <div class="relative z-1 max-w-[62rem] mx-auto text-center mb-[4rem] md:mb-20 lg:mb-[6rem]">
                <h1 class="h1 mb-6">
                    Explore the Possibilites of AI Chatting with
                    <span class="inline-block relative">
                        Brainwave
                        <img 
                            :src="curve"
                            alt="Curve"
                            class="absolute top-full left-0 w-full xl:-mt-2"
                            width="624px"
                            height="2px"
                        >
                    </span>
                </h1>
                <p class="body-1 max-w-3xl mx-auto mb-6 text-n-2 lg:mb-8">
                    Unleash the power of AI within Brainwave. Upgrade your productivity
                    with Brainwave, the open AI chat app.
                </p>
                <Button 
                    href="/pricing" 
                    color="white"
                >
                    Get started
                </Button>
            </div>

            <div class="relative max-w--[23rem] mx-auto md:max-w-5xl xl:mb-24">
                <div class="relative z-1 p-0.5 rounded-2xl bg-conic-gradient">
                    <div class="relative bg-n-8 rounded-[1rem]">
                        <div class="h-[1.4rem] bg-n-10 rounded-t-[0.9rem]" />
                        <div class="aspect-[33/40] rounded-b-[0.9rem] overflow-hidden md:aspect-[688/490] lg:aspect-[1024/490]">
                            <img 
                                :src="robot" 
                                alt="Robot"
                                class="w-full scale-[1.7] transalte-y-[80%] md:scale-[1] md:-translate-y-[10%] lg:-translate-y-[23%]"
                                width="1024px"
                                height="490px"                            
                            >
                            <Generating
                                className="absolute left-4 right-4 bottom-5 md:left-1/2 md:right-auto md:bottom-8 md:w-[31rem] md:-translate-x-1/2"
                             />
                            <div>
                                <ul class="hidden absolute -left-[5.5rem] bottom-[7.5rem] px-1 py-1 bg-n-9/40 backdrop-blur border border-n-1/10 rounded-2xl xl:flex">
                                    <li 
                                        v-for="(icon, index) in heroIcons" 
                                        :key="index"
                                        class="p-5"
                                    >
                                        <img 
                                            :src="icon" 
                                            :alt="icon" 
                                            width="24px" 
                                            height="25px"
                                        >
                                    </li>
                                </ul>
                            </div>
                            <div>
                                <Notification 
                                    className="hidden absolute -right-[5.5rem] bottom-[11rem] w-[18rem] xl:flex"
                                    title="Code Generation"
                                />
                            </div>
                        </div>
                    </div>
                    <DesignHeroGradient />
                </div>

                <div class="absolute -top-[54%] left-1/2 w-[234%] -translate-x-1/2 md:-top-[64%] md:w-[138%] lg:-top-[104%]">
                    <img 
                        :src="heroBackground" 
                        alt="Hero"
                        class="w-full"
                        width="1440px"
                        height="1800px"
                    >
                </div>
                <DesignHeroBackgroundCircles />
            </div>
            <CompanyLogos className="hidden relative z-10 mt-20 lg:block" />
        </div>
        <DesignHeroBottomLine />
    </SectionBase>
</template>

<script setup>
import { useParallax } from '@vueuse/core'

import { heroIcons }  from '~/utils/constant'
import { curve, heroBackground, robot } from '~/assets'

const container = ref(null)
useParallax(container)
</script>