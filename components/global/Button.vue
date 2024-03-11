<template>
   <button :class="[
      color ? 'text-n-8' : 'text-n-1',className, px || 'px-7',
      'btn-base'
    ]"
    v-if="!href"
    @click="$emit('toggleNavigation')"
  >
    <slot />
    <span class="relative z-10">
      {{ children }}
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
  <slot />
    <span class="relative z-10">
      {{ children }}
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
  