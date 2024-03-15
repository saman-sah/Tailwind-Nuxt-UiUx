<template>
  <div :class="[
    className,
    'max-w-[50rem] mx-auto mb-12 lg:mb-20 md:text-center'
  ]"
  >
    <TagLine v-if="tag" 
      className="mb-4 md:justify-center"
    >
      Get started wuth brainwave
    </TagLine>
    <h2
      v-if="title"
      class="h2 md:text-center"
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
import TagLine from './TagLine.vue'
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
  },
  tag: {
    type: String,
    default: ''
  }
})
</script>