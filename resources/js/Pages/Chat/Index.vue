<script setup>
import MainLayout from "@/Layouts/MainLayout.vue";

const props = defineProps([
   'users',
]);

</script>

<template>
    <MainLayout>
        <div class="flex w-full h-[calc(100vh-64px)] overflow-hidden bg-white">

            <!-- Левая часть, поиск, колонка с чатами -->

            <aside class="w-1/3 border-r border-gray-200 flex flex-col bg-gray-50">
                <div class="h-16 p-4">
                    <input type="text" placeholder="Поиск..." class="w-full rounded-lg border-gray-300 focus:ring-indigo-500 focus:border-indigo-500 text-sm">
                </div>

                <div class="flex-1 overflow-y-auto">
                    <div v-for="user in users.data" :key="user.id" class="flex items-center p-4 hover:bg-indigo-50 cursor-pointer border-b border-gray-100 transition">
                        <div class="w-12 h-12 bg-indigo-200 rounded-full flex-shrink-0 flex items-center justify-center font-bold text-indigo-700">
                            {{ user.name.charAt(0).toUpperCase() }}
                        </div>
                        <div class="ml-4 overflow-hidden">
                            <p class="text-sm font-medium text-gray-900">{{ user.name }}</p>
                            <p class="text-xs text-gray-500 truncate">Последнее сообщение из чата...</p>
                        </div>
                    </div>
                </div>
            </aside>

            <!-- Конец левой части, поиск, колонка с чатами -->

            <!-- Блок чата -->

            <section class="flex-1 flex flex-col">
                <div class="h-16 px-6 border-b flex items-center justify-between shadow-sm">
                    <h2 class="font-semibold">Чат с пользователем</h2>
                </div>

                <div class="flex-1 p-6 overflow-y-auto bg-gray-100 flex flex-col gap-3">
                    <div class="bg-white p-3 rounded-lg shadow-sm max-w-md self-start">
                        Привет ! Как дела ?
                    </div>
                    <div class="bg-indigo-600 text-white p-3 rounded-lg shadow-sm max-w-md self-end">
                        Привет, все отлично
                    </div>
                </div>

                <div class="p-4 border-t bg-white">
                    <div class="flex gap-2">
                        <input type="text" placeholder="Напишите сообщение"
                               class="flex-1 border-gray-300 rounded-full px-4 focus:ring-indigo-500 focus:border-indigo-500">
                        <button
                            class="bg-indigo-600 text-white px-6 py-2 rounded-full hover:bg-indigo-700 transition">
                            Отправить
                        </button>
                    </div>
                </div>
            </section>
            <!-- Конец блока чата -->

        </div>
    </MainLayout>
</template>

<style scoped>

</style>
