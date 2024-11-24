<script setup lang="ts">
const { type = 'text', ...props } = defineProps([
    'type',
    'placeholder'
])

const model = defineModel()
</script>

<template>
    <input :type="type" :placeholder="props.placeholder" v-model="model" class="mb-8 rounded-3xl py-2 px-5 custom-input w-full" />
</template>

<style scoped>
.custom-input {
    background: #f4f4f4;
    stroke: #e8e8e8;
}
</style>