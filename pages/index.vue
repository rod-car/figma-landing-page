<template>
    <CustomSection
        id="feature-section"
        title="Features"
        subtitle="Most calendars are designed for teams. Slate is designed for freelancers"
    >
        <div class="grid gap-4 items-start grid-cols-1 my-16 md:grid-cols-3 md:my-16">
            <Item title="OpenType features Variable fonts" icon="images/features/open_type.png">
                Slate helps you see how many more days you need to work to reach your financial goal.
            </Item>

            <Item title="Design with real data" icon="images/features/design.png">
                Slate helps you see how many more days you need to work to reach your financial goal.
            </Item>

            <Item title="Fastest way to take action" icon="images/features/action.png">
                Slate helps you see how many more days you need to work to reach your financial goal.
            </Item>
        </div>

        <div class="flex items-center justify-center">
            <video class="text-center w-auto rounded-lg" controls>
                <source
                    src="https://docs.material-tailwind.com/demo.mp4"
                    type="video/mp4"
                />
                Your browser does not support the video tag.
            </video>
        </div>
    </CustomSection>

    <CustomSection id="">
        <div class="grid gap-16 items-center grid-cols-1 md:grid-cols-2">
            <div class="flex flex-col items-center md:block">
                <h2 class="mb-5 font-normal text-center md:text-left">Fastest way to organize</h2>
                <h4 class="text-center md:text-left">Most calendars are designed for teams. Slate is designed for freelancers</h4>
                <ActionButton class="mt-10">Try for free</ActionButton>
            </div>
            <NuxtImg class="h-auto w-full bg-cover" src="/images/computer.png" />
        </div>
    </CustomSection>

    <CustomSection>
        <div class="grid gap-16 items-center grid-cols-1 md:grid-cols-2">
            <NuxtImg class="h-auto w-full bg-cover" src="/images/left-container.png" />
            <div>
                <div class="mb-7">
                    <h3 class="text-base font-bold">At your fingertips</h3>
                    <h2 class="font-normal">Lightning fast prototyping </h2>
                </div>

                <div class="mb-10">
                    <h3 class="text-base font-bold">Subscribe to our Newsletter</h3>
                    <p class="font-normal">Available exclusivery on Figmaland</p>
                </div>

                <Input type="email" placeholder="Your email" class="me-5" />
                <Button class="rounded-3xl">Subscribe</Button>
            </div>
        </div>
    </CustomSection>

    <CustomSection
        title="Partners"
        subtitle="Most calendars are designed for teams. Slate is designed for freelancers"
    >
        <div class="grid grid-cols-4 items-start my-16">
            <PartnerCard name="Google" logo="images/partners/logo_google.png" />
            <PartnerCard name="Amazon" logo="images/partners/logo_amazon.png" />
            <PartnerCard name="Microsoft" logo="images/partners/logo_microsoft.png" />
            <PartnerCard name="Uber" logo="images/partners/logo_uber.png" />
            <PartnerCard name="Dropbox" logo="images/partners/logo_dropbox.png" />
            <PartnerCard name="Google" logo="images/partners/logo_google.png" />
            <PartnerCard name="Amazon" logo="images/partners/logo_amazon.png" />
            <PartnerCard name="Microsoft" logo="images/partners/logo_microsoft.png" />
        </div>
        <div class="flex justify-center">
            <ActionButton class="mx-auto">Try for free</ActionButton>
        </div>
    </CustomSection>

    <CustomSection title="Testimonials">
        <TestimonialBlock
            logo="images/testimonials/logo_ibm.png"
            message="Most calendars are designed for teams. Slate is designed for freelancers"
            avatar="images/testimonials/avatar.png"
            organization="Organize across"
            role="Ui designer"
        />

        <div class="flex justify-center">
            <ActionButton class="mx-auto">More testimonials</ActionButton>
        </div>
    </CustomSection>

    <CustomSection
        class="custom-section"
        id="pricing-section"
        title="Pricing"
        subtitle="Most calendars are designed for teams. Slate is designed for freelancers"
    >
        <div class="grid gap-10 items-center mt-10 grid-cols-1 md:grid-cols-3">
            <PricingCard
                title="Free"
                :price="0"
                description="Organize across all apps by hand"
                :features="[
                    'Pricing feature',
                    'Pricing feature',
                    'Pricing feature',
                    'Pricing feature',
                    'Pricing feature'
                ]"
                action="Order now"
            />

            <PricingCard
                title="Standard"
                :price="10"
                :recommended="true"
                description="Organize across all apps by hand"
                :features="[
                    'Pricing feature',
                    'Pricing feature',
                    'Pricing feature',
                    'Pricing feature',
                    'Pricing feature'
                ]"
                action="Order now"
            />

            <PricingCard
                title="Enterprise"
                :price="99"
                description="Organize across all apps by hand"
                :features="[
                    'Pricing feature',
                    'Pricing feature',
                    'Pricing feature',
                    'Pricing feature',
                    'Pricing feature'
                ]"
                action="Order now"
            />
        </div>
    </CustomSection>

    <CustomSection
        title="Contact Us"
        id="contact-section"
        subtitle="Most calendars are designed for teams. Slate is designed for freelancers"
    >
        <div class="grid gap-16 items-start mt-8 grid-cols-1 md:grid-cols-3">
            <div class="shadow-2xl rounded-2xl p-8 md:col-span-1 bg-white">
                <h3 class="mb-7 text-center">Contact Us</h3>
                <form method="post" @submit.prevent="sendMessage">
                    <Input v-model="formData.name" placeholder="Your name" />
                    <Input v-model="formData.email" type="email" placeholder="Your email" />
                    <Textarea v-model="formData.message" placeholder="Your message" />

                    <span class="block text-green-600 pb-3" v-if="status === 2">Message envoye</span>
                    <span class="block text-red-600 pb-3" v-if="status === 3">Message non envoye</span>

                    <Button :class="status === 1 && 'opacity-50 pointer-events-none'" type="submit">Send</Button>
                </form>
            </div>

            <div class="p-3 md:col-span-2">
                <div class="md:flex md:justify-between md:items-start">
                    <ContactInfo
                        icon="images/contact/location.png"
                        value="6386 Spring St undefined Anchorage, Georgia 12473 United States"
                    />
                    <ContactInfo
                        icon="images/contact/phone.png"
                        value="(843) 555-0130"
                        :nowrap="true"
                    />
                    <ContactInfo
                        icon="images/contact/email.png"
                        value="willie.jennings@example.com"
                    />
                </div>
                <div class="my-8 flex items-center justify-center">
                    <NuxtImg class="w-1/2" src="images/contact/map.png" />
                </div>
                <PrimarySocialMedias />
            </div>
        </div>
    </CustomSection>
</template>

<script setup lang="ts">

import PartnerCard from "~/components/Card/PartnerCard.vue";
import ActionButton from "~/components/Structure/ActionButton.vue";
import PricingCard from "~/components/Card/PricingCard.vue";
import ContactInfo from "~/components/Structure/ContactInfo.vue";
import PrimarySocialMedias from "~/components/Structure/PrimarySocialMedias.vue";
import TestimonialBlock from "~/components/Structure/TestimonialBlock.vue";
import Item from "~/components/Structure/Item.vue";
import CustomSection from "~/components/Structure/CustomSection.vue";
import Input from "~/components/Form/Input.vue";
import Textarea from "~/components/Form/Textarea.vue";
import Button from "~/components/Form/Button.vue";

const formData = ref({
    access_key: "245dcfd5-e9f1-409d-af2f-a2a7d470455a",
    subject: "New Submission from Web3Forms",
    name: "Carino",
    email: "ghislaincarino@gmail.com",
    message: "Teste de message",
})

const status = ref(0) // default to idle

const sendMessage = async () => {
    try {
        status.value = 1 // Loading

        await $fetch('https://api.web3forms.com/submit', {
            method: 'POST',
            headers: { 'Content-Type': 'application/json' },
            body: formData.value,
        });

        status.value = 2 // sent
    } catch (error) {
        status.value = 3 // Not sent
    }
}
</script>

<style>
.custom-section {
    background: #252B42;
    color: white;
}
</style>