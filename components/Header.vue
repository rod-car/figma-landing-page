<script setup lang="ts">

import NavLink from "~/components/Structure/NavLink.vue";
import FigmaLogo from "~/components/Structure/FigmaLogo.vue";
import SocialMedias from "~/components/Structure/SocialMedias.vue";
import ActionButton from "~/components/Structure/ActionButton.vue";
import { ref, computed, onMounted, onUnmounted } from "vue";

let scrollY = ref(0);
const isMenuOpen = ref(false); // État pour afficher/masquer le menu sur mobile
const classes = computed(() => (scrollY.value > 0 ? "custom-navbar" : ""));

const toggleMenu = () => {
    isMenuOpen.value = !isMenuOpen.value;
};

const handleScroll = () => {
    scrollY.value = window.scrollY;
    if (isMenuOpen.value === true) isMenuOpen.value = false
};

onMounted(() => {
    scrollY.value = window.scrollY;
    window.addEventListener("scroll", handleScroll);
});

onUnmounted(() => {
    window.removeEventListener("scroll", handleScroll);
});
</script>

<template>
    <header class="px-8 md:p-0 backgrounder-header" id="home-section">
        <nav class="text-white fixed left-0 right-0" :class="classes">
            <div class="md:px-36" id="navbar">
                <div class="flex flex-wrap items-center justify-between py-2 px-4 md:py-4 md:px-0 relative">
                    <ul
                        class="absolute md:static flex-1 top-full left-0 right-0 flex-col items-center bg-gray-800 md:flex md:flex-row md:space-x-8 md:bg-transparent rtl:space-x-reverse"
                        :class="{
                            hidden: !isMenuOpen && !$attrs.class?.includes('md:flex'),
                            flex: isMenuOpen || $attrs.class?.includes('md:flex'),
                        }"
                    >
                        <NavLink href="#home-section">Home</NavLink>
                        <NavLink href="#feature-section">Product</NavLink>
                        <NavLink href="#pricing-section">Pricing</NavLink>
                        <NavLink href="#about-section">About</NavLink>
                        <NavLink href="#contact-section">Contact</NavLink>
                    </ul>

                    <!-- Logo (Centre pour grand écran) -->
                    <div class="flex-1 md:flex md:items-center md:justify-center">
                        <FigmaLogo />
                    </div>

                    <button
                        class="md:hidden text-white"
                        @click="toggleMenu"
                        aria-label="Toggle Menu"
                    >
                        <svg
                            class="w-6 h-6"
                            fill="none"
                            stroke="currentColor"
                            viewBox="0 0 24 24"
                            xmlns="http://www.w3.org/2000/svg"
                        >
                            <path
                                stroke-linecap="round"
                                stroke-linejoin="round"
                                stroke-width="2"
                                d="M4 6h16M4 12h16m-7 6h7"
                            ></path>
                        </svg>
                    </button>

                    <div class="hidden md:flex-1 md:flex md:items-center md:justify-end">
                        <SocialMedias />
                    </div>
                </div>
            </div>
        </nav>

        <div class="py-0 h-screen flex flex-col justify-center items-center">
            <h1 class="text-center text-5xl text-white mb-5">The best products start with Figma</h1>
            <h4 class="text-center text-white">
                Most calendars are designed for teams. Slate is designed for freelancers
            </h4>
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
    transition: all 0.5s;
}
</style>
