<script setup>
import { Link } from '@inertiajs/vue3';


</script>

<template>
    <div class="min-h-screen flex flex-col">
        <nav class="bg-indigo-700 text-white shadow-lg px-6 py-4 flex items-center gap-8">
                <div class="font-bold text-xl tracking-tight">Laravel Chat</div>
                <div class="font-bold text-xl tracking-tight">
                    <Link :href="route('chats.index')" class="hover:text-indigo-200 transition">Chats</Link>
                </div>
        </nav>

        <main class="flex-1 flex overflow-hidden">
            <slot />
        </main>
    </div>
</template>

<style scoped>

</style>
