<script setup lang="ts">
const props = defineProps({
    name: String,
    logo: String
})
</script>

<template>
    <div class="flex justify-center items-center p-2.5 md:p-5 flex-col">
        <h6 class="mb-3">{{props.name}}</h6>
        <NuxtImg class="w-full md:w-1/2" :src="logo" />
    </div>
</template>