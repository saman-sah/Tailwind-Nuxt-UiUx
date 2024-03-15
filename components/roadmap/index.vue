<template>
  <SectionBase
    className="overflow-hidden"
    id="roadmap"
  >
    <div class="container md:pb-10">
      <Heading
        tag="Ready to get started"
        title="What we're working on"
      />
      <div class="relative grid gap-6 md:grid-cols-2 md:gap-4 md:pb-[7rem]">
        <div
          v-for="item in roadmap"
          :key="item.id"
          :class="[
            item.colorful ? 'bg-conic-gradient' : 'bg-n-6',
            'md:flex even:translate-y-[7rem] p-0.25 rounded-[2.5rem]'
          ]"
        >
          <div class="relative p-8 bg-n-8 rounded-[2rem] overflow-hidden xl:p-15">
            <div class="absolute top-0 left-0 max-w-full">
              <img 
                :src="grid" 
                alt="grid"
                class="w-full"
                width="550px"
                height="550px"
              >
            </div>
            <div class="relative z-1">
              <div class="flex items-center justify-between max-w-[27rem] mb-8 md:mb-20">
                <TagLine>
                  {{ item.date }}
                </TagLine>
                <div class="flex items-center px-4 py-1 bg-n-1 rounded text-n-8">
                  <img 
                    :src="item.status === 'done' ? check2 : loading1" 
                    :alt="item.status"
                    class="mr-2.5"
                    width="16px"
                    height="16px"
                  >
                  <div class="tagline">
                    {{ item.status }}
                  </div>
                </div>

                <div class="mb-10 -my-10 -mx-15">
                  <img 
                    :src="item.imageUrl" 
                    :alt="item.title"
                    width="630px"
                    height="420px"
                    class="w-full"
                  >
                </div>
                <h4 class="h4 mb-4">
                  {{ item.title }}
                </h4>
                <p class="body-2 text-n-4">
                  {{ item.text }}
                </p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </SectionBase>
</template>

<script setup>
import { check2, grid, loading1 } from '~/assets';
import Heading from './Heading.vue';
import { roadmap } from '~/utils/constant'
import TagLine from './TagLine.vue';

</script>