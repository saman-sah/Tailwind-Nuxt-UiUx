<template>
  <SectionBase
    crosses
    crossesOffset="lg:translate-y-[5.25rem]"
  >
    <div class="container lg:flex">
      <div class="max-w-[25rem]">
        <h2 class="h2 mb-4 md:mb-8">
          AI Chat App for seamless collaboration
        </h2>
        <ul class="max-w-[22rem] mb-10 md:mb-14">
          <li
            v-for="collab in collabContent"
            :key="collab.id"
            class="mb-3 py-3"
          >
            <div class="flex items-center">
              <img 
                :src="check"
                width="24px"
                height="24px"
                alt="check"
              >
              <h6 class="body-2 ml-5">
                {{ collab.title }}
              </h6>
            </div>
            <p 
              v-if="collab.text"
              class="body-2 mt-3 text-n-4"
            >
              {{ collab.text }}
            </p>
          </li>
        </ul>

        <Button>
          Tri it now
        </Button>

      </div>

      <div class="lg:ml-auto xl:w-[38rem] mt-4">
        <p class="body-2 mb-8 text-n-4 md:mb-16 lg:mb-32 lg:w-[22rem] lg:mx-auto">
          {{ collabText }}
        </p>

        <div class="mt-4 relative left-1/2 flex w-[22rem] aspect-square border border-n-6 rounded-full -translate-x-1/2 scale:75 md:scale-100">
          <div class="flex w-60 aspect-square m-auto border border-n-6 rounded-full">
            <div class="w-[6rem] aspect-square m-auto p-[0.2rem] bg-conic-gradient rounded-full">
              <div class="flex items-center justify-center w-full h-full bg-n-8 rounded-full">
                <img 
                  :src="brainwaveSymbol" 
                  alt="brainwave"
                  width="48px"
                  height="48px"
                >
              </div>
            </div>
          </div>
          <ul>
            <li
              v-for="(app, index) in collabApps"
              :key="app.id"
              :class="[
                `rotate-${index*45}`,
                'absolute top-0 left-1/2 h-1/2 -ml-[1.6rem] origin-bottom'
              ]"
            >
              <div :class="[
                `-rotate-${index*45}`,
                'relative -top-[1.6rem] flex w-[3.2rem] h-[3.2rem] bg-n-7 border border-n-1/5 rounded-xl'
              ]">
                <img 
                  :src="app.icon" 
                  :alt="app.title"
                  class="m-auto"
                  :width="app.width"
                  :height="app.height"
                >
              </div>
            </li>
          </ul>
          <LeftCurve />
          <RightCurve />
        </div>
      </div>

    </div>
  </SectionBase>
</template>

<script setup>
import { check, brainwaveSymbol } from '~/assets'
import { 
  collabContent, 
  collabText,
  collabApps
} from '~/utils/constant'

import LeftCurve from '../design/collaboration/LeftCurve.vue'
import  RightCurve from '../design/collaboration/RightCurve.vue'
</script>
