<template>
  <div class="absolute -top-[42.375rem] left-1/2 w-[78rem] aspect-square border border-n-2/5 rounded-full -translate-x-1/2 md:-top-[38.5rem] xl:-top-[32rem]">
    <DesignHeroRings />


    <MouseParallax strength={0.07} parallaxContainerRef={parallaxRef}>
      <div class="absolute bottom-1/2 left-1/2 w-0.25 h-1/2 origin-bottom rotate-[46deg]">
        <div
          :class="[
            mount ? 'translate-y-0 opacity-100' : 'translate-y-10 opacity-0',
            'w-2 h-2 -ml-1 -mt-36 bg-gradient-to-b from-[#DD734F] to-[#1A1A32] rounded-full transition-transform duration-500 ease-out'
          ]"
        />
      </div>

      <div class="absolute bottom-1/2 left-1/2 w-0.25 h-1/2 origin-bottom -rotate-[56deg]">
        <div
          :class="[
            mount ? 'translate-y-0 opacity-100' : 'translate-y-10 opacity-0',
            'w-4 h-4 -ml-1 -mt-32 bg-gradient-to-b from-[#DD734F] to-[#1A1A32] rounded-full transition-transform duration-500 ease-out'
          ]"
        />
      </div>

      <div class="absolute bottom-1/2 left-1/2 w-0.25 h-1/2 origin-bottom rotate-[54deg]">
        <div
          :class="[
            mount ? 'translate-y-0 opacity-100' : 'translate-y-10 opacity-0',
            'hidden w-4 h-4 -ml-1 mt-[12.9rem] bg-gradient-to-b from-[#B9AEDF] to-[#1A1A32] rounded-full xl:block transit transition-transform duration-500 ease-out'
          ]"
        />
      </div>

      <div class="absolute bottom-1/2 left-1/2 w-0.25 h-1/2 origin-bottom -rotate-[65deg]">
        <div
          :class="[
            mount ? 'translate-y-0 opacity-100' : 'translate-y-10 opacity-0',
            'w-3 h-3 -ml-1.5 mt-52 bg-gradient-to-b from-[#B9AEDF] to-[#1A1A32] rounded-full transition-transform duration-500 ease-out'
          ]"
        />
      </div>

      <div class="absolute bottom-1/2 left-1/2 w-0.25 h-1/2 origin-bottom -rotate-[85deg]">
        <div
          :class="[
            mount ? 'translate-y-0 opacity-100' : 'translate-y-10 opacity-0',
            'w-6 h-6 -ml-3 -mt-3 bg-gradient-to-b from-[#88E5BE] to-[#1A1A32] rounded-full transition-transform duration-500 ease-out'
          ]"
        />
      </div>

      <div class="absolute bottom-1/2 left-1/2 w-0.25 h-1/2 origin-bottom rotate-[70deg]">
        <div
          :class="[
            mount ? 'translate-y-0 opacity-100' : 'translate-y-10 opacity-0',
            'w-6 h-6 -ml-3 -mt-3 bg-gradient-to-b from-[#88E5BE] to-[#1A1A32] rounded-full transition-transform duration-500 ease-out'
          ]"
        />
      </div>
    </MouseParallax>
  </div>

</template>

<script setup>
import { useParallax } from '@vueuse/core'
const mount = ref(false)

const circle1 = ref(null);
const circle2 = ref(null);
const circle3 = ref(null);
const circle4 = ref(null);
const circle5 = ref(null);
const circle6 = ref(null);

onMounted(() => {
  useParallax(circle1, { strength: 0.07 });
  useParallax(circle2, { strength: 0.07 });
  useParallax(circle3, { strength: 0.07 });
  useParallax(circle4, { strength: 0.07 });
  useParallax(circle5, { strength: 0.07 });
  useParallax(circle6, { strength: 0.07 });

  // Set mounted flag to true after mounting
  mount.value = true;
});
</script>