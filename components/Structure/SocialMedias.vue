<script setup lang="ts">
const {color = 'text-white'} = defineProps({
    color: String
})
</script>

<template>
    <div class="flex flex-wrap items-center justify-end">
        <NuxtLink href="#" target="_blank" class="me-2"><NuxtImg class="w-full md:w-8/12" :class="color" src="images/social/twitter.svg" alt="Twitter"/></NuxtLink>
        <NuxtLink href="#" target="_blank" class="me-2"><NuxtImg class="w-full md:w-8/12" src="images/social/facebook.svg" alt="Facebook"/></NuxtLink>
        <NuxtLink href="#" target="_blank"><NuxtImg class="w-8/12" src="images/social/linkedin.svg" alt="Linkedin"/></NuxtLink>
    </div>
</template>

<style scoped>
.text-primary {
    color: #2091F9;
}
</style>