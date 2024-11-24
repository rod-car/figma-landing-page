<script setup lang="ts">

import NavLink from "~/components/Structure/NavLink.vue";
import FigmaLogo from "~/components/Structure/FigmaLogo.vue";
import SocialMedias from "~/components/Structure/SocialMedias.vue";
import ActionButton from "~/components/Structure/ActionButton.vue";
import {computed} from "vue";

let scrollY = ref(0)
const classes = computed(() => scrollY.value > 0 ? 'custom-navbar' : '')

const handleScroll = () => {
    scrollY.value = window.scrollY
}

onMounted(() => {
    scrollY.value = window.scrollY
    window.addEventListener('scroll', handleScroll)
})

onUnmounted(() => {
    window.removeEventListener('scroll', handleScroll)
})

</script>

<template>
    <header class="px-8 md:p-0 backgrounder-header" id="home-section">
        <nav class="text-white fixed left-0 right-0" :class="classes">
            <div class="md:px-36 md:block md:w-auto" id="navbar">
                <div class="flex flex-wrap items-center justify-between px-8 py-2 md:py-4">
                    <ul class="hidden flex-1 text-white font-medium md:flex flex-col items-center p-4 md:p-0 mt-4 rounded-lg md:flex-row md:space-x-8 rtl:space-x-reverse md:mt-0">
                        <NavLink href="#home-section">Home</NavLink>
                        <NavLink href="#feature-section">Product</NavLink>
                        <NavLink href="#pricing-section">Pricing</NavLink>
                        <NavLink href="#about-section">About</NavLink>
                        <NavLink href="#contact-section">Contact</NavLink>
                    </ul>
                    <div class="md:flex md:justify-center">
                        <FigmaLogo />
                    </div>
                    <div class="md:flex-1">
                        <SocialMedias />
                    </div>
                </div>
            </div>
        </nav>

        <div class="py-0 h-screen flex flex-col justify-center items-center">
            <h1 class="text-center text-5xl text-white mb-5">The best products start with Figma</h1>
            <h4 class="text-center text-white">Most calendars are designed for teams. Slate is designed for freelancers</h4>
            <ActionButton class="mt-16">Try for free</ActionButton>
        </div>
    </header>
</template>

<style scoped>
.backgrounder-header {
    background-image: url("/images/background.png");
    background-size: cover;
    background-position: bottom;
}

.custom-navbar {
    background: rgba(37, 43, 66, 0.8);
    transition: all;
    transition-duration: .5s;
}
</style>