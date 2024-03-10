<template>
  <NuxtLink :class="[
      white ? 'text-n-8' : 'text-n-1',
      'btn-base'
    ]"
    :to="href"
    v-if="href.length"
  >
  Btn Link
    <span class="">
      {{ children }}
    </span>
    <ButtonSvg :color="color" />
  </NuxtLink>
  

  <button :class="[
      white ? 'text-n-8' : 'text-n-1',
      'btn-base'
    ]"
    v-else
  >
  Btn Def
    <span class="">
      {{ children }}
    </span>
    <ButtonSvg :color="color" />
  </button>
  
  
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
  