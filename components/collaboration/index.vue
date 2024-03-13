<template>
  <SectionBase
    crosses
    crossesOffset="lg:translate-y-[5.25rem]"
  >
  {{ collabContent }}
    <div class="container lg:flex">
      <div class="max-w-[25rem]">
        <h2 class="h2 mb-4 md:mb-8">
          AI Chat App for seamless collaboration
        </h2>
        <ul class="max-w-[22rem] mb-10 md:mb-14">
          <li
            v-for="collab in collabContent"
            :key="collab.id"
          >
            <div class="flex items-center">
              <img 
                :src="check"
                width="24px"
                height="24px"
                alt="check"
              >
              <h6 class="body-2 ml-5">
                {{ item.title }}
              </h6>
              <p 
                v-if="collab.text"
                class="body-2 mt-3 text-n-4"
              >
                {{ item.text }}
              </p>
            </div>
          </li>
        </ul>
      </div>
    </div>
  </SectionBase>
</template>

<script setup>
import { check } from '~/assets'
import collabContent from '~/utils/constant'

console.log('collabContent', collabContent);
</script>
