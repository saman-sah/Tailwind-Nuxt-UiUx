<template>
   <button :class="[
      color ? 'text-n-8' : 'text-n-1',className, px || 'px-7',
      'btn-base'
    ]"
    v-if="!href"
    @click="$emit('toggleNavigation')"
  >
    <span class="relative z-50">
      <slot />
    </span>
    <ButtonSvg :color="color" />
  </button>
  
  <NuxtLink :class="[
      color ? 'text-n-8' : 'text-n-1',className, px || 'px-8',
      'btn-base'
    ]"
    :to="href"
    v-else
  >
  
    <span class="relative z-10">
      <slot />
    </span>
    <ButtonSvg :color="color" />
  </NuxtLink>
  

  
</template>

<script setup>
import { ButtonSvg } from '~/assets/svg'

defineProps({
  className: {
    type: String,
    default: ''
  },
  onClick: {

  },
  children: {

  },
  px: {

  },
  href: {
    type: String,
    default: ''
  },
  color: {
    type: String,
    default: ''
  }
})
</script>
  