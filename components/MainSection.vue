<template>
    <div class="border-x" :class="twitterBorderColor">
        <!-- begin ::: title ::: -->
        <div class="sticky top-0 px-4 py-3 bg-white/80 backdrop-blur-md dark:bg-dim-900/80">
            <h2 class="text-xl font-bold text-gray-800 dark:text-gray-100">{{ title }}</h2>
        </div>
        <!-- end ::: title ::: -->
        <div
            v-if="loading"
            class="flex items-center justify-center p-4 border-b"
            :class="twitterBorderColor"
        >
            <UISpinner/>
        </div>
        <div v-else>
            <slot/>
        </div>
    </div>
</template>
<script lang="ts" setup>
const {twitterBorderColor} = useTailwindConfig()

interface PorpsInterface {
    title: string,
    loading: boolean,
}

defineProps<PorpsInterface>()
</script>
