<script setup>
import { Head, Link } from '@inertiajs/vue3';
import MainMenu from "@/Components/MainMenu.vue";

defineProps({
    canLogin: Boolean,
    canRegister: Boolean,
    laravelVersion: String,
    phpVersion: String,
});
</script>

<template>
    <Head title="Welcome" />

    <MainMenu canLogin canRegister />

</template>
