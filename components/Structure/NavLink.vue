<script setup lang="ts">
const props = defineProps({
    href: String
})

</script>

<template>
    <li class="w-full text-center md:w-auto">
        <NuxtLink :href="props.href" class="primary-link block py-2 px-3 rounded md:border-0 md:p-0">
            <slot />
        </NuxtLink>
    </li>
</template>

<style scoped>
.primary-link:hover {
    color: #2091F9!important;
}
</style>