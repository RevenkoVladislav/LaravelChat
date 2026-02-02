<script setup>
import { Link } from '@inertiajs/vue3';


</script>

<template>
    <div class="min-h-screen bg-gray-100 flex flex-col">
        <nav class="bg-indigo-700 text-white shadow-lg px-6 py-4">
            <div class="max-w-7xl mx-auto flex justify-between items-center">
                <div class="font-bold text-xl tracking-tight">Laravel Chat</div>
                <div class="flex gap-4">
                    <Link :href="route('chats.index')" class="hover:text-indigo-200 transition">Chats</Link>
                </div>
            </div>
        </nav>

        <main class="flex-1 flex overflow-hidden">
            <slot />
        </main>
    </div>
</template>

<style scoped>

</style>
