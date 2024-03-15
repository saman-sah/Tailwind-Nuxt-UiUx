<template>
  <svg
    class="overflow-visible"
    width="20"
    height="12"
    viewBox="0 0 20 12"
  >
    <rect
      class="transition-all origin-center"
      :style="{'y':openNavigation ? '-5' : '0'}"
      width="20"
      height="2"
      rx="1"
      fill="white"
      :transform="openNavigation ? 'rotate(45)' : 'rotate(0)'"
    />
    <rect
      class="transition-all origin-center"
      :style="{'y':openNavigation ? '10' : '10', 'x':openNavigation ? '-5' : '0'}"
      width="20"
      height="2"
      rx="1"
      fill="white"
      :transform="openNavigation ? 'rotate(-45)' : 'rotate(0)'"
    />
  </svg>
</template>

<script setup>
defineProps({
  openNavigation: { 
    type: Boolean ,
    default: false
  }
});
</script>