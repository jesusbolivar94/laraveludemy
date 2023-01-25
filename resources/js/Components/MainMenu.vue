<script setup>

    import { Link } from '@inertiajs/vue3';

    defineProps({
        canLogin: Boolean,
        canRegister: Boolean,
    })

</script>

<template>
    <div v-if="canLogin" class="hidden fixed top-0 right-0 px-6 py-4 sm:block">
        <Link
            v-if="$page.props.auth.user"
            :href="route('dashboard')"
            class="text-sm text-gray-700 dark:text-gray-500 underline"
        >Dashboard</Link>

        <template v-else>
            <Link :href="route('login')" class="text-sm text-gray-700 dark:text-gray-500 underline">Log in</Link>

            <Link
                v-if="canRegister"
                :href="route('register')"
                class="ml-4 text-sm text-gray-700 dark:text-gray-500 underline"
            >Register</Link>
        </template>

        <Link :href="route('about')" class="ml-4 text-sm text-gray-700 dark:text-gray-500 underline">About</Link>
        <Link :href="route('blog')" class="ml-4 text-sm text-gray-700 dark:text-gray-500 underline">Blog</Link>
        <Link :href="route('contact')" class="ml-4 text-sm text-gray-700 dark:text-gray-500 underline">Contact</Link>

    </div>
</template>
