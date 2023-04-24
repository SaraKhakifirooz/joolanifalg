<template>
    <div>
        <header class="bg-green-100 p-2">
            <div class="wrapper">
                <nav class="w-100 py-2 md:py-4">
                    <div class="container px-4 mx-auto md:flex md:items-center">

                        <div class="flex justify-between items-center">
                            <button
                                class="border border-solid border-green-600 px-3 py-1 rounded text-green-600 opacity-50 hover:opacity-75 md:hidden"
                                id="navbar-toggle">
                                <i class="fas fa-bars"></i>
                            </button>
                        </div>

                        <div class="hidden md:flex flex-col md:flex-row md:ml-auto mt-3 md:mt-0" id="navbar-collapse">
                            <RouterLink
                                class="p-2 lg:px-4 md:mx-2 text-green-600 rounded hover:bg-green-200 hover:text-green-700 transition-colors duration-300"
                                to="/">Home</RouterLink>
                            <RouterLink
                                class="p-2 lg:px-4 md:mx-2 text-green-600 rounded hover:bg-green-200 hover:text-green-700 transition-colors duration-300"
                                to="/about">About</RouterLink>

                        </div>
                    </div>
                </nav>

            </div>
            <img alt="Vue logo" class="logo" src="@/assets/logo.svg" width="80" />


        </header>
    </div>
</template>


<script setup lang="ts">

// import { RouterLink, RouterView } from 'vue-router'

</script>