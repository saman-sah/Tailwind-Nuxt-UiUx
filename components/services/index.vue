<template>
  <SectionBase
    id="how-to-use"    
  >
    <div class="container">
      <HeadingServices 
        title="Generative AI made for creators"
        text="Brainwave unlocks the potential of AI-powered applications"
      />
      <div class="relative">
        <div class="relative z-1 flex items-center h-[39rem] mb-5 p-8 border border-n-1/10 rounded-3xl overflow-hidden lg:p-20 xl:h-[46rem]">
          <div class="absolute top-0 left-0 w-full h-full pointer-events-none md:w-3/5 xl:w-auto">
            <img 
              :src="service1" 
              alt="Smartest AI"
              class="w-full h-full object-cover md:object-right"
              width="800px"
              height="730px"
            >
          </div>
          <div class="relative z-1 max-w-[17rem] ml-auto">
            <h4 class="h4 mb-4">
              Smartest AI
            </h4>            
            <p class="body-2 mb-[3rem] text-n-3">
              Brainwave unlocks the potential of AI-powered aoolications
            </p>
            <ul class="body-2">
              <li 
                v-for="(item, index) in brainwaveServices"
                :key="index"
                class="flex items-start py-4 border-t border-n-6"
              >
                <img 
                  :src="check" 
                  alt=""
                  width="24px"
                  height="24px"
                >
                <p class="ml-4">
                  {{ item }}
                </p>
              </li>
            </ul>
          </div>
          <Generating
            className="absolute left-4 right-4 bottom-4 border border-n-1/10 lg:left-1/2 lg-right-auto lg:bottom-8 lg:-translate-x-1/2" 
          />
        </div>

        <div class="relative z-1 grid gap-5 lg:grid-col-2">
          <div class="relative min-h-[39rem] border border-n-1/10 rounded-3xl overflow-hidden">
            <div class="absolute inset-0">
              <img :src="service2" 
                alt="robot"
                class="h-full w-full object-cover"
                width="600px"
                height="750px"
              >
            </div>
            <div class="absolute inset-0 flex flex-col justify-end p-8 bg-gradient-to-b from-n-8/0 to-n-8/90 lg:p-15">
              <h4 class="h4 mb-4">
                Photo editing
              </h4>            
              <p class="body-2 mb-[3rem] text-n-3">
                Automaticlly enhance your photos using our AI app's photo editing feature. Try it now!
              </p>
            </div>

            <DesignServicesPhotoChatMessage />

          </div>
          <div class="p-4 bg-n-7 rounded-3xl overflow-hidden lg:min-h-[46rem]">
            <div class="py-12 px-4 xl:px-8">
              <h4 class="h4 mb-4">
                Video Generation
              </h4>
              <p class="body-2 mb-[2rem] text-n-3">
                The world's most powerful AI photo and video art generation engine.What will you create?
              </p>
              <ul class="flex items-center justify-between">
                <li 
                  v-for="(item, indexIcon) in brainwaveServicesIcons"
                  :key="indexIcon"
                  :class="[
                    indexIcon === 2 
                    ? 'w-[3rem] h-[3rem] p-0.5 bg-conic-gradient md:w-[4.5rem] md:h-[4.5rem]' 
                    : 'flex w-10 h-10 bg-n-6  md:w-15 md:h-15',
                    'flex items-center justify-center rounded-2xl'
                  ]"
                >
                  <div :class="[
                    indexIcon === 2 ? 'flex items-center justify-center w-full h-full bg-n-7 rounded-[1rem]' : ''
                    ]"
                  >
                    <img 
                      :src="item" 
                      alt="Brainwave Service Icon"
                      width="24px"
                      height="24px"
                    >
                  </div>
                </li>
              </ul>
            </div>

            <div class="relative h-[20rem] bg-n-8 rounded-xl overflow-hidden md:h-[25rem]">
              <img 
                :src="service3" 
                alt="Scary Robot" 
                class="w-full h-full object-cover"
                width="520px"
                height="400px"
              >
              <DesignServicesVideoChatMessage />
              <DesignServicesVideoBar />
            </div>

          </div>
        </div>

        <DesignServicesGradient />

      </div>
    </div>
  </SectionBase>
</template>

<script setup>
import HeadingServices from './Heading.vue'
import { check, service1, service2, service3 } from '~/assets'
import { brainwaveServices, brainwaveServicesIcons } from '~/utils/constant'
import Generating from '../Generating.vue'
</script>