<template>
  <div class="absolute left-0 bottom-0 w-full flex items-center p-6">
    <img
      :src="play"
      width="24px"
      height="24px"
      alt="Play"
      class="object-contain mr-3"
    />

    <div class="flex-1 bg-[#D9D9D9]">
      <div class="w-1/2 h-0.5 bg-color-1"></div>
    </div>
  </div>
</template>

<script setup>
import { play } from '~/assets'
</script>