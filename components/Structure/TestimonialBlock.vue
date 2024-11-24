<script setup lang="ts">
const props = defineProps({
    logo: String,
    avatar: String,
    message: String,
    organization: String,
    role: String
})
</script>

<template>
    <div class="my-10 flex flex-col justify-center items-center">
        <NuxtImg class="w-1/4" :src="props.logo" />
        <h4 class="text-center py-10">{{props.message}}</h4>

        <div class="flex flex-row items-center justify-center">
            <NuxtImg class="w-1/4" :src="props.avatar" />
            <div class="ms-3">
                <h6 class="text-nowrap">{{props.organization}}</h6>
                <NuxtLink href="#">{{props.role}}</NuxtLink>
            </div>
        </div>
    </div>
</template>