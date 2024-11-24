<template>
    <footer class="px-10 py-8 md:py-20 md:px-40 grid grid-cols-2 md:grid-cols-5 bg-dark">
        <div class="mb-8 md:mb-0">
            <h3 class="mb-3 md:mb-5">Pages</h3>
            <ul>
                <li class="mb-2"><NuxtLink href="#">Home</NuxtLink></li>
                <li class="mb-2"><NuxtLink href="#">Product</NuxtLink></li>
                <li class="mb-2"><NuxtLink href="#">Pricing</NuxtLink></li>
                <li class="mb-2"><NuxtLink href="#">About</NuxtLink></li>
                <li class="mb-2"><NuxtLink href="#">Contact</NuxtLink></li>
            </ul>
        </div>
        <div class="mb-8 md:mb-0">
            <h3 class="mb-3 md:mb-5">Tomothy</h3>
            <ul>
                <li class="mb-2"><NuxtLink href="#">Eleanor Edwards</NuxtLink></li>
                <li class="mb-2"><NuxtLink href="#">Ted Robertson</NuxtLink></li>
                <li class="mb-2"><NuxtLink href="#">Annette Russel</NuxtLink></li>
                <li class="mb-2"><NuxtLink href="#">Jennie Mckinney</NuxtLink></li>
                <li class="mb-2"><NuxtLink href="#">Gloria Richards</NuxtLink></li>
            </ul>
        </div>
        <div>
            <h3 class="mb-3 md:mb-5">Jane Black</h3>
            <ul>
                <li class="mb-2"><NuxtLink href="#">Philip Jones</NuxtLink></li>
                <li class="mb-2"><NuxtLink href="#">Product</NuxtLink></li>
                <li class="mb-2"><NuxtLink href="#">Colleen Russell</NuxtLink></li>
                <li class="mb-2"><NuxtLink href="#">Marvin Hawkins</NuxtLink></li>
                <li class="mb-2"><NuxtLink href="#">Bruce Simmons</NuxtLink></li>
            </ul>
        </div>
        <div class="md:col-span-2 flex items-start flex-col md:px-16">
            <div class="flex items-center justify-center mb-5">
                <NuxtImg src="images/contact/location_white.png" class="w-8 me-3" />
                <p>7480 Mockingbird Hill undefined</p>
            </div>
            <div class="flex items-start mb-5">
                <NuxtImg src="images/contact/phone_white.png" class="w-5 me-3" />
                <p>(239) 555-0108</p>
            </div>
            <SocialMedias />
        </div>
    </footer>
</template>

<style scoped>
.bg-dark {
    background: #252B42; color: white;
}
</style>
<script setup lang="ts">
import SocialMedias from "~/components/Structure/SocialMedias.vue";
</script>