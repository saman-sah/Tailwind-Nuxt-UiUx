<template>
   <button :class="[
      color ? 'text-n-8' : 'text-n-1',className || '',
      'btn-base'
    ]"
    v-if="!href"
  >
  Btn Def
    <span class="relative z-10">
      {{ children }}
    </span>
    <ButtonSvg class="ddddddddddd" :color="color" />
  </button>
  
  <NuxtLink :class="[
      white ? 'text-n-8' : 'text-n-1',
      'btn-base'
    ]"
    :to="href"
    v-else
  >
  Btn Link
    <span class="">
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
  