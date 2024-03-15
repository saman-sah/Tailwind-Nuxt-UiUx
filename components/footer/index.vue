<template>
  <SectionBase
    id="footer"
    className="!px-0 !py-10"
  >
    <div class="container flex sm:justify-between justify-center items-center gap-10 max-sm:flex-col">
      <p class="captioon text-n-4 lg:block">
        © {{new Date().getFullYear()}}. All rights reserved.
      </p>
      <ul class="flex gap-5 flex-wrap">
          <NuxtLink 
            v-for="(social, index) in socials"
            :key="index"
            :to="social.url"
            target="_blank"
            class="flex items-center justify-center w-10 h-10 bg-n-7 rounded-full transition-colors hover:bg-n-6"
          >
            <img 
              :src="social.iconUrl" 
              :alt="social.title"
              width="16px"
              height="16px"
            >
          </NuxtLink>
      </ul>
    </div>
  </SectionBase>
</template>

<script setup>
</script>