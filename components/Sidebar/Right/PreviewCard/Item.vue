<template>
  <div
          class="p-3 border-b cursor-pointer hover:bg-gray-100 dark:hover:bg-dim-300 dark:text-gray-400"
          :class="classWrapper"
  >
   <slot />
  </div>
</template>
<script lang="ts" setup>
const { defaultTransition, twitterBorderColor } = useTailwindConfig()

const classWrapper = computed(() => `${defaultTransition} ${twitterBorderColor}`)
</script>
