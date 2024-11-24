<template>
    <button class="custom-btn py-1.5 px-8 rounded-3xl md:font-bold">
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
    color: #2091F9;
    background: white;
    border-color: #2091F9;
}
</style>
