<template>
  <SectionBase
    className="overflow-hidden"
    id="pricing"
  >
    <div class="container relative z-2">
      <div class="hidden relative justify-center mb-[6.5rem] lg:flex">
        <img 
          :src="smallSphere" 
          class="relative z-1"
          width="255px"
          height="255px"
          alt="Sphere"
        >
        <div class="absolute top-1/2 left-1/2 w-[60rem] -translate-x-1/2 -translate-y-1/2 pointer-events-none">
          <img 
            :src="stars" 
            alt="Stars"
            class="w-full"
            width="950px"
            height="400px"
          >
        </div>
      </div>
      <Heading 
        tag="Get started with Brainwave"
        title="Pay once, use forever"
      />

      <div class="relative">
        <PricingList />
      </div>
    </div>
  </SectionBase>
</template>

<script setup>
import { stars,smallSphere } from '~/assets';
import Heading from './Heading.vue'
import PricingList from './PricingList.vue'


</script>