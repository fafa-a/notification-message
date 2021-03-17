<template>
  <div class="flex">
    <div class="m-auto w-96">
      <div
        class="relative p-3 border border-gray-300 rounded-lg shadow-lg"
        :class="type"
        v-if="!hidden"
      >
        <div class="flex flex-row">
          <div class="ml-2 mr-6">
            <div :class="type" v-if="!hidden">
              <span
                class="absolute top-1 right-1 p-0.5 cursor-pointer font-bold text-xs"
                @click="hide"
                >X</span
              >
              <span class="block">{{ header }}</span>
              <slot></slot>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { defineProps, ref } from "vue";

defineProps({
  type: {
    type: String,
    default: "info",
  },
  header: {
    type: String,
    default: "Information",
  },
});

const hidden = ref(false);
const hide = () => {
  hidden.value = true;
};
</script>

<style lang="postcss">
.error {
  @apply bg-red-200 text-red-600;
}

.success {
  @apply bg-green-200 text-green-600;
}

.info {
  @apply text-blue-400;
}
</style>
