<template>
  <PlusSvg
    :className="crossesOffset + 'hidden absolute -top-[0.3125rem] left-[1.5625rem] pointer-events-none lg:block xl:left-[2.1875rem]'"
  />

  <PlusSvg
    :className="crossesOffset + 'hidden absolute  -top-[0.3125rem] right-[1.5625rem] pointer-events-none lg:block xl:right-[2.1875rem]'"
  />
</template>

<script setup>
import PlusSvg from "./PlusSvg.vue"

defineProps({
  crossesOffset: {
    type: String,
    default: ''
  }
})
</script>