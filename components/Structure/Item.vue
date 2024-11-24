<script setup lang="ts">
const props = defineProps({
    title: String,
    icon: String
})
</script>

<template>
    <div class="flex flex-col items-center justify-center">
        <NuxtImg :src="props.icon" alt="Icon" class="mb-5 h-1/2" />
        <h3 class="text-center">{{props.title}}</h3>
        <p class="text-center">
            <slot />
        </p>
    </div>
</template>