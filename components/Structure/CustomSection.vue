<script setup lang="ts">
const props = defineProps({
    title: String,
    subtitle: String
})
</script>

<template>
    <section class="flex flex-col items-center justify-center py-8 px-10 md:py-32 md:px-36">
        <h2 v-if="props.title" class="mb-7 font-normal">{{props.title}}</h2>
        <h4 v-if="props.subtitle" class="mb-7">{{props.subtitle}}</h4>
        <slot />
    </section>
</template>