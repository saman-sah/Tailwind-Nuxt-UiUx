<template>
    <div
      :class="[
        className,
        'flex items-center p-4 pr-6 bg-n-9/40 backdrop-blur border border-n-1/10 rounded-2xl gap-5'
      ]"
    >
      <img
        :src="notification1"
        width="62px"
        height="62px"
        alt="image"
        class="rounded-xl"
      />

      <div class="flex-1">
        <h6 class="mb-1 font-semibold text-base">{{  title }}</h6>

        <div class="flex items-center justify-between">
          <ul class="flex -m-0.5">
              <li
                v-for="(item, index) in notificationImages"
                :key="index"
                class="flex w-6 h-6 border-2 border-n-12 rounded-full overflow-hidden"
              >
                <img
                  :src="item"
                  class="w-full"
                  width="20px"
                  height="20px"
                  :alt="item"
                />
              </li>
          </ul>
          <div class="body-2 text-n-13">1m ago</div>
        </div>
      </div>
    </div>
</template>

<script setup>
import { notification1 } from "~/assets";
import { notificationImages } from "~/utils/constant"

defineProps({
  className: {
    type: String,
    default: ''
  },
  title: {
    type: String,
    default: ''
  }
})
</script>