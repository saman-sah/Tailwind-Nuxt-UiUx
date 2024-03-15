<template>
  <SectionBase 
    id="features"
  >
    <div class="container relative z-2">
      <BenefitsHeading
        className=""
        title="Chat Smarter. Not Harder with Brainwave"
      />
      <div class="flex flex-wrap gap-10 mb-10">
        <div
          v-for="benefit in benefits"
          :key="benefit.id"
          class="block relative p-0.5 bg-no-repeat bg-[length:100%_100%] md:max-w-[24rem]"
          :style="{backgroundImage: 'url(' + benefit.backgroundUrl + ')'}"
        >
          <div class="relative z-2 flex flex-col min-h-[22rem] p-[2.4rem] pointer-events-none">
            <h5 class="h5 mb-5">
              {{ benefit.title }}
            </h5>
            <p class="body-2 mb-6 text-n-3">
              {{ benefit.text }}
            </p>
            <div class="flex items-center mt-auto">
              <img 
                :src="benefit.iconUrl"
                width="48px"
                height="48px"
                :alt="benefit.title"
              >
              <p class="ml-auto font-code text-xs font-bold text-n-1 uppercase tracking-wider">
                Explore more
              </p>
              <Arrow />
            </div>
          </div>
          <BenefitsGradientLight v-if="benefit.light" />

          <div
            :style="{ clipPath: 'url(#benefits)'}"
            class="absolute inset-0.5 bg-n-8"
          >
            <div 
              v-if="benefit.imageUrl"
              class="absolute inset-0.5 opacity-0 transition-opacity hover:opacity-10"
            >
              <img 
                :src="benefit.imageUrl" 
                :alt="benefit.title"
                width="380px"
                height="362px"
                class="w-full h-full object-cover"
              >
            </div>
          </div>
          <ClipPath />
        </div>
      </div>
    </div>
  </SectionBase>
</template>

<script setup>
import { benefits } from '~/utils/constant'

import Arrow from '~/assets/svg/Arrow.vue'
import ClipPath from '~/assets/svg/ClipPath.vue'
</script>
