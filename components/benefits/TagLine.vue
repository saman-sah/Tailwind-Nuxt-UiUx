<template>
  <div
    :class="[
      className,
      'tagline flex items-center'
    ]"
  >
    <Brackets position="left" />
    <div class="mx-3 text-n-3">
      <slot />
    </div>
    <Brackets position="right" />
  </div>
</template>

<script setup>
import Brackets from "~/assets/svg/Brackets.vue"

defineProps({
  className: {
    type: String,
    default: ''
  }
})
</script>