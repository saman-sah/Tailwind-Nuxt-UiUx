<template>
  <div class="flex gap-[1rem] max-lg:flex-wrap">
    <div 
      v-for="item in pricing"
      :key="item.id"
      class="w-[19rem] max-lg:w-full h-full px-6 bg-n-8 border border-n-6 rounded-[2rem] lg:w-auto even:py-14 odd:py-8 odd:my-4 [&>h4]:first:text-color-2 [&>h4]:even:text-color-1 [&>h4]:last:text-color-3"
    >
      <h4 class="h4 mb-4">
        {{ item.title }}
      </h4>
      <p class="body-2 min-h-[4rem] mb-3 text-n-1/50">
        {{ item.description }}
      </p>
      <div
        v-if="item.price"
        class="flex items-center h-[5.5rem] mb-6"
      >
        <div class="h3">$</div>
        <div class="text-[5.5rem] leading-none font-bold">
          {{ item.price }}
        </div>
      </div>
      <Button
        className="w-full mb-6"
        :to="item.price ? '/pricing' : 'mailto:contact@mydite.pro'"
        :color="!!item.price ? 'white' : ''"
      >
        {{ item.price ? 'Get Started' : 'Contact Us' }}
      </Button>
      <ul>
        <li
          v-for="(feature, index) in item.features"
          :key="index"
          class="flex items-start py-5 border-t border-n-6"
        >        
          <img
            :src="check" 
            alt="Check"
            width="24px"
            height="24px"
          >
          <p class="body-2 ml-4">
            {{ feature }}
          </p>
        </li>
      </ul>
    </div>
  </div>
</template>

<script setup>
import { check } from '~/assets'
import { pricing } from '~/utils/constant'
</script>