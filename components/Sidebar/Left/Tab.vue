<template>
<nuxt-link to="#" class="flex items-center rounded-full p-3 w-min text-black hover:bg-gray-200 dark:hover:bg-dim-200 dark:text-white">
   <div
           class="w-6 h-6 text-dark"
           :class="defaultTransition"
   >
       <slot name="icon"/>
   </div>
   <div class="hidden ml-4 text-xl xl:block" :class="textClasses">
       <slot name="name"/>
   </div>
</nuxt-link>
</template>
<script lang="ts" setup>
const { defaultTransition } = useTailwindConfig()

interface PropsInterface{
    active?: boolean
}
const props = withDefaults(defineProps<PropsInterface>(),{
    active: false
})

const textClasses = computed(() => {
    return props.active ? 'font-semibold' : 'font-normal'
})
</script>