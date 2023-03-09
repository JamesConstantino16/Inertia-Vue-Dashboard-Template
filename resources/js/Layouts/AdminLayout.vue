<script setup>
import { ref } from 'vue';
import ApplicationLogo from '@/Components/ApplicationLogo.vue';
import Dropdown from '@/Components/Dropdown.vue';
import DropdownLink from '@/Components/DropdownLink.vue';
import ResponsiveNavLink from '@/Components/ResponsiveNavLink.vue';
import MainMenu from '@/Components/MainMenu.vue'
import { Link } from '@inertiajs/vue3';

import { ChevronDownIcon } from '@heroicons/vue/24/outline'

const showingNavigationDropdown = ref(false);
</script>

<template>
    <div>
        <div class="md:flex md:flex-col bg-gradient-to-b from-primary-700 via-primary-700 to-primary-900">
            <div class="md:flex md:flex-col md:h-screen">
                <div class="md:flex md:flex-shrink-0">
                    <div
                        class="flex items-center justify-between px-6 py-4 md:flex-shrink-0 md:justify-center md:w-64 border-b border-primary-600">
                        <Link class="flex items-center mt-1" :href="route('dashboard')">
                        <ApplicationLogo class="block h-9 w-auto fill-current text-white mr-2" />
                        <div class="text-xl text-white">Dashboard</div>
                        </Link>
                        <dropdown class="md:hidden" placement="bottom-end">
                            <template #default>
                                <svg class="w-6 h-6 fill-white" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20">
                                    <path d="M0 3h20v2H0V3zm0 6h20v2H0V9zm0 6h20v2H0v-2z" />
                                </svg>
                            </template>
                            <template #dropdown>
                                <div class="mt-2 px-8 py-4 bg-primary-800 rounded shadow-lg">
                                    <Dropdown align="right" width="48">
                                        <template #trigger>
                                            <span class="inline-flex rounded-md">
                                                <button type="button"
                                                    class="inline-flex items-center px-3 py-2 border border-transparent text-sm leading-4 font-medium rounded-md text-gray-500 dark:text-gray-400 bg-white dark:bg-gray-800 hover:text-gray-700 dark:hover:text-gray-300 focus:outline-none transition ease-in-out duration-150">
                                                    {{ $page.props.auth.user.name }}

                                                    <ChevronDownIcon class="h-6 w-6" />
                                                </button>
                                            </span>
                                        </template>

                                        <template #content>
                                            <DropdownLink :href="route('profile.edit')"> Profile </DropdownLink>
                                            <DropdownLink :href="route('logout')" method="post" as="button">
                                                Log Out
                                            </DropdownLink>
                                        </template>
                                    </Dropdown>
                                </div>
                            </template>
                        </dropdown>
                    </div>
                    <div
                        class="md:text-md flex items-center justify-between p-4 w-full text-sm bg-white border-b md:px-12 md:py-0">
                        <div class="mr-4 mt-1">{{ $page.props.auth.user.name }} Corporation</div>
                        <div class="hidden md:flex sm:items-center sm:ml-6">
                            <!-- Settings Dropdown -->
                            <div class="ml-3 text-white relative">
                                <Dropdown align="right" width="48">
                                    <template #trigger>
                                        <span class="inline-flex rounded-md">
                                            <button type="button"
                                                class="inline-flex items-center px-3 py-2 text-sm leading-4 font-medium rounded-md text-gray-500 dark:text-gray-400 bg-white dark:bg-gray-800 hover:text-gray-700 dark:hover:text-gray-300 focus:outline-none transition ease-in-out duration-150">
                                                {{ $page.props.auth.user.name }}

                                                <ChevronDownIcon class="h-4 w-4 ml-2" />
                                            </button>
                                        </span>
                                    </template>

                                    <template #content>
                                        <DropdownLink :href="route('profile.edit')"> Profile </DropdownLink>
                                        <DropdownLink :href="route('logout')" method="post" as="button">
                                            Log Out
                                        </DropdownLink>
                                    </template>
                                </Dropdown>
                            </div>
                        </div>

                        <!-- Hamburger -->
                        <div class="-mr-2 flex items-center md:hidden">
                            <button @click="showingNavigationDropdown = !showingNavigationDropdown"
                                class="inline-flex items-center justify-center p-2 rounded-md text-gray-400 dark:text-gray-500 hover:text-gray-500 dark:hover:text-gray-400 hover:bg-gray-100 dark:hover:bg-gray-900 focus:outline-none focus:bg-gray-100 dark:focus:bg-gray-900 focus:text-gray-500 dark:focus:text-gray-400 transition duration-150 ease-in-out">
                                <svg class="h-6 w-6" stroke="currentColor" fill="none" viewBox="0 0 24 24">
                                    <path :class="{
                                        hidden: showingNavigationDropdown,
                                        'inline-flex': !showingNavigationDropdown,
                                    }" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                        d="M4 6h16M4 12h16M4 18h16" />
                                    <path :class="{
                                        hidden: !showingNavigationDropdown,
                                        'inline-flex': showingNavigationDropdown,
                                    }" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                        d="M6 18L18 6M6 6l12 12" />
                                </svg>
                            </button>
                        </div>
                    </div>
                    <!-- Responsive Navigation Menu -->
                    <div :class="{ block: showingNavigationDropdown, hidden: !showingNavigationDropdown }"
                        class="sm:hidden">
                        <div class="pt-2 pb-3 text-white space-y-1">
                            <ResponsiveNavLink :href="route('dashboard')" :active="route().current('dashboard')">
                                Dashboard
                            </ResponsiveNavLink>
                        </div>

                        <!-- Responsive Settings Options -->
                        <div class="pt-4 pb-1 border-t border-gray-200 dark:border-gray-600 active:bg-primary-800">
                            <div class="px-4">
                                <div class="font-medium text-base text-gray-800 dark:text-gray-200">
                                    {{ $page.props.auth.user.name }}
                                </div>
                                <div class="font-medium text-sm text-gray-500">{{ $page.props.auth.user.email }}</div>
                            </div>

                            <div class="mt-3 text-white space-y-1">
                                <ResponsiveNavLink :href="route('profile.edit')"> Profile </ResponsiveNavLink>
                                <ResponsiveNavLink :href="route('logout')" method="post" as="button">
                                    Log Out
                                </ResponsiveNavLink>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="md:flex md:flex-grow md:overflow-hidden">
                    <div
                        class="hidden flex-shrink-0 py-4 w-64 overflow-y-auto md:block">
                        <MainMenu />
                    </div>
                    <div class="bg-gray-100 h-full px-2 py-8 md:flex-1 md:p-8 md:overflow-y-auto">
                        <!-- <flash-messages /> -->
                        <slot />
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
