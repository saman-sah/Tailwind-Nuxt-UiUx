<template>
  <div :class="[className]">
    <h5 class="tagline mb-6 text-center text-n-1/50">
      Helping people create beautiful content at
    </h5>
    <ul class="flex">
      <li
        v-for="(logo, index) in companyLogos"
        class="flex items-center justify-center flex-1 h-[8.5rem]"
        :key="index"
      >
        <img 
          :src="logo" 
          width="134px"
          height="28px"
          :alt="logo" 
        />
      </li>
    </ul>
  </div>
</template>

<script setup>
import { companyLogos } from "~/utils/constant"

defineProps({
  className: String,
  default: ''
})
</script>