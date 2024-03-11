<template>
  <div :class="[
    customPaddings || 'py-10 lg:py-16 xl:py-20',
    !crosses || 'lg:py-32 xl:py-40',
    className || '',
      'relative'
    ]"
  >

  </div>
</template>

<script setup>
​defineProps({
  className: {
    type: String,
    default: ''
  },
  crosses: {
    type: String,
    default: ''
  },
  crossesOffset: {
    type: String,
    default: ''
  },
  customPaddings: {
    type: String,
    default: ''
  }
});
</script>
