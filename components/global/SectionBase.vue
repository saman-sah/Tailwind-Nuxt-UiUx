<template>
  <div :class="[
      className,
      customPaddings || `py-10 lg:py-16 xl:py-20 ${crosses ? 'lg:py-32 xl:py-40' : ''}`,
      'relative'
    ]"
    :id="id"
  >
    <slot />
    <div class="hidden absolute top-0 left-5 w-0.25 h-full bg-stroke-1 pointer-events-none md:block lg:left-7.5 xl:left-10" />
    <div class="hidden absolute top-0 right-5 w-0.25 h-full bg-stroke-1 pointer-events-none md:block lg:right-7.5 xl:right-10" />

    <div
      v-if="crosses"
      :class="[
        crossesOffset,
        'hidden absolute top-0 left-7.5 right-7.5 h-0.25 bg-stroke-1 pointer-events-none lg:block xl:left-10 xl:right-10'
      ]"
    />
    <SectionSvg :crossesOffset="crossesOffset" />
  </div>
</template>

<script setup>
import SectionSvg from '~/assets/svg/SectionSvg.vue';

defineProps({
  className: {
    type: String,
    default: ''
  },
  crosses: {
    type: Boolean,
    default: true
  },
  crossesOffset: {
    type: String,
    default: ''
  },
  customPaddings: {
    type: String,
    default: ''
  },
  id: {
    type: String,
    default: ''
  }
});
</script>
