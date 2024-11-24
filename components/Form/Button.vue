<script setup lang="ts">
const {type = 'button'} = defineProps([
    'type'
])
</script>

<template>
    <button type="submit" class="custom-btn rounded-3xl py-1.5 px-8 md:font-bold">
        <slot />
    </button>
</template>

<style scoped>
.custom-btn {
    background: #2091F9;
    color: white;
    border: 1px solid #2091F9;
}

.custom-btn:hover {
    background: white;
    color: #2091F9;
    border-color: #2091F9;
}
</style>