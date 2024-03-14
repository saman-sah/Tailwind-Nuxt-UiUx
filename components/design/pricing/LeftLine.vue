<template>
  <div class="hidden lg:block absolute top-1/2 right-full w-[92.5rem] h-[11.0625rem] -translate-y-1/2 pointer-events-none">
    <img
      class="w-full"
      :src="lines"
      width="1480px"
      height="177px"
      alt="Lines"
    />
  </div>
</template>

<script setup>
import { lines } from "./assets"
</script>
