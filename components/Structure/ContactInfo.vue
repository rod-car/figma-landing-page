<script setup lang="ts">
const props = defineProps({
    icon: String,
    value: String,
    nowrap: Boolean
})
</script>

<template>
    <div class="p-3 flex flex-col items-center justify-start flex-auto">
        <NuxtImg :src="props.icon" class="mb-2" />
        <p class="text-center" :class="props.nowrap && 'text-nowrap'">
            {{props.value}}
        </p>
    </div>
</template>

<style scoped>

</style>