<script setup lang="ts">

import ActionButton from "~/components/Structure/ActionButton.vue";

const { unit = '$', period = 'Month', recommended = false, ...props } = defineProps({
    title: String,
    recommended: Boolean,
    description: String,
    features: Array,
    action: String,
    price: Number,
    unit: String,
    period: String
})
</script>

<template>
    <div class="rounded p-5 bg-white text-black text-center" :class="recommended && 'py-16 recommended'">
        <div class="p-4">
            <h3 class="fw-bold uppercase mb-3">{{props.title}}</h3>
            <h6>{{props.description}}</h6>

            <div class="grid grid-cols-2 gap-4 items-center my-3">
                <h1 class="text-end mb-0">{{props.price}}</h1>
                <div>
                    <h6 class="text-start font-bold">{{unit}}</h6>
                    <h6 class="text-start">Per {{period}}</h6>
                </div>
            </div>

            <ul class="mt-5">
                <li class="p-2" v-for="(item, index) in props.features" :key="index">
                    {{ item }}
                </li>
            </ul>
        </div>

        <ActionButton class="w-full rounded-3xl" :class="recommended && 'recbtn'">{{props.action}}</ActionButton>
    </div>
</template>

<style scoped>
.recommended {
    background: #2091F9;
    color: white;
    border: 1px solid white;
}

.recbtn {
    color: #2091F9;
    background: white;
}

.recbtn:hover {
    color: white;
    background: #2091F9;
    border: 1px solid white;
}
</style>