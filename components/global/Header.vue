<template>
  <section id="hearder">
    <div class="fixed top-0 left-0 w-full z-50 bg-n-8/90 backdrop-blur-sm border-b border-n-6">
      <div class="flex items-center px-5 lg:px-7.5 xl:px-10 max-lg:py-4">

        <NuxtLink class="block w-[12rem] xl:mr-8" to="#hero">
          <img :src="brainwave" width="190px" height="40px" alt="Brainwave" />
        </NuxtLink>

        <div class="flex flex-row justify-between w-full">
          <nav class="hidden fixed top-[5rem] left-0 right-0 bottom-0 bg-n-8 lg:static lg:flex lg:max-auto lg:bg-transparent">
            <div class="relative z-2 flex flex-col items-center justify-between m-auto lg:flex-row">            
              <NuxtLink 
                v-for="(item, index) in navigation"
                :key="index"
                :class="[
                  !item.onlyMobile || 'lg:hidden', route.hash === item.url ? 'z-2 lg:text-n-1' : 'lg:text-n-1/50',
                  'block lg:leading-5 lg:hover:text-n-1 xl:px-12 relative font-code text-2xl uppercase text-n-1 px-6 py-6 md:py-8 lg:-mr-0.25 lg:text-xs lg:font-semibold transition-colors hover:text-color-1'
                ]"
                :to="item.url"
              >
                {{ item.title }}
              </NuxtLink>
            </div>
          </nav>
          <div class="flex items-center">
            <NuxtLink 
            to="#signup"
            class="button hidden mr-8 text-n-1/50 transition-colors hover:text-n-1 lg:block"
          >
            New Acoount
          </NuxtLink>
          <Button class="hidden lg:flex" href="#login" >
            Sign Up
          </Button>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { brainwave } from '~/assets';
import { navigation } from '~/utils/constant';

const route = useRoute()

console.log('route', route.hash);
</script>
