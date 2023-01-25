<script setup>
    import { Head } from '@inertiajs/vue3'

    import GuestLayout from '@/Layouts/GuestLayout.vue'
    import MainMenu from "@/Components/MainMenu.vue";
</script>

<template>

    <GuestLayout>

        <Head title="Blog"/>

        <MainMenu canLogin canRegister />

        <p class="text-white">Blog</p>

    </GuestLayout>

</template>
