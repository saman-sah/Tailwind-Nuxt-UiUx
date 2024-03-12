<template>
  <div
    :class="[
      className,
      'flex items-center h-[3.5rem] px-6 bg-n-8/80 rounded-[1.7rem] text-base'
    ]"
  >
    <img 
      class="w-5 h-5 mr-4" 
      :src="loading" 
      alt="Loading" 
    />
    AI is generating
  </div>
</template>

<script setup>
import { loading } from "../assets"
defineProps({
  className: {
    type: String,
    default: ''
  }
})
</script>