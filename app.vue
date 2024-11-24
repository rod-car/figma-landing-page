<template>
    <div class="m-0 h-full">
        <NuxtRouteAnnouncer />
        <Header />
        <NuxtPage />
        <Footer />
    </div>
</template>

<script setup lang="ts">
useSeoMeta({
    title: "FIGMA Landing Page",
    description: "Figma community landing page"
})
</script>
