<script setup>
import { ref } from 'vue';

const isMenuOpen = ref(false); // État du menu
</script>

<template>
    <nav class="bg-white border-gray-200 dark:bg-gray-900">
        <div class="max-w-screen-xl flex flex-wrap items-center justify-between mx-auto p-4">
            <!-- Bouton Hamburger -->
            <button class="md:hidden" @click="isMenuOpen = !isMenuOpen">
                <span class="material-symbols-outlined">
                    menu
                </span> </button>

            <!-- Menu -->
            <div :class="{ 'block': isMenuOpen, 'hidden': !isMenuOpen }" class="w-full md:block md:w-auto"
                id="navbar-default">
                <ul
                    class="font-medium flex flex-col p-4 md:p-0 mt-4 border border-gray-100 rounded-lg bg-gray-50 md:flex-row md:space-x-8 rtl:space-x-reverse md:mt-0 md:border-0 md:bg-white dark:bg-gray-800 md:dark:bg-gray-900 dark:border-gray-700">
                    <li>
                        <RouterLink to="/"
                            class="block py-2 px-3 text-white bg-blue-700 rounded md:bg-transparent md:text-blue-700 md:p-0 dark:text-white md:dark:text-blue-500"
                            aria-current="page">Accueil</RouterLink>
                    </li>
                    <li>
                        <RouterLink to="/about"
                            class="block py-2 px-3 text-gray-900 rounded hover:bg-gray-100 md:hover:bg-transparent md:border-0 md:hover:text-blue-700 md:p-0 dark:text-white md:dark:hover:text-blue-500 dark:hover:bg-gray-700 dark:hover:text-white md:dark:hover:bg-transparent">
                            A propos</RouterLink>
                    </li>
                </ul>
            </div>
        </div>
    </nav>
</template>
