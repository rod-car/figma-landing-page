<script setup lang="ts">
const props = defineProps([
    'placeholder'
])

const model = defineModel()
</script>

<template>
    <textarea :placeholder="props.placeholder" v-model="model" rows="4" class="mb-8 rounded py-2 px-5 custom-input w-full"></textarea>
</template>

<style scoped>
.custom-input {
    background: #f4f4f4;
    stroke: #e8e8e8;
}
</style>