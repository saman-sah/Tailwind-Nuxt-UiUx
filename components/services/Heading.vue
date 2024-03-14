<template>
  <div :class="[
    className,
    'max-w-[50rem] mx-auto mb-12 lg:mb-20'
  ]"
  >
    <h2
      v-if="title"
      class="h2"
    >
      {{ title }}
    </h2>
    <p
      v-if="text" 
      class="body-2 mt-4 text-n-4"
    >
      {{ text }}
    </p>
  </div>
</template>

<script setup>
defineProps({
  className: {
    type: String,
    default: ''
  },
  title: {
    type: String,
    default: ''
  },
  text: {
    type: String,
    default: ''
  }
})
</script>