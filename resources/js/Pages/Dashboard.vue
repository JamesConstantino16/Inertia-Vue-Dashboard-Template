<script setup>
import AdminLayout from '@/Layouts/AdminLayout.vue';
import { Head } from '@inertiajs/vue3';

import { ArrowUpIcon } from '@heroicons/vue/24/outline'
import { ArrowDownIcon } from '@heroicons/vue/24/outline'
import { ShoppingCartIcon } from '@heroicons/vue/24/outline'
</script>

<template>
    <Head title="Dashboard" />

    <AdminLayout>
        <div class="max-w-7xl mx-auto sm:px-4 lg:px-6 space-y-6">
            <h3 class="text-lg font-medium leading-6 text-gray-900">
                Last 30 days
            </h3>
            <dl
                class="grid grid-cols-1 mt-5 overflow-hidden bg-white divide-y divide-gray-200 rounded-lg shadow md:grid-cols-3 md:divide-y-0 md:divide-x">
                <div class="px-4 py-5 sm:p-6">
                    <dt class="text-base font-normal text-gray-900">
                        Product Name
                    </dt>
                    <dd class="flex items-baseline justify-between mt-1 md:block lg:flex">
                        <div class="flex items-baseline text-2xl font-semibold text-primary-600">
                            Stats
                            <span class="ml-2 text-sm font-medium text-gray-500">from 0</span>
                        </div>

                        <div class="inline-flex items-baseline px-2.5 py-0.5 rounded-full text-sm font-medium md:mt-2 lg:mt-0">
                            <ArrowUpIcon class="-ml-1 mr-0.5 h-5 w-5 flex-shrink-0 self-center text-green-500"
                                aria-hidden="true" />
                            <ArrowDownIcon class="-ml-1 mr-0.5 h-5 w-5 flex-shrink-0 self-center text-red-500"
                                aria-hidden="true" />
                            <span class="sr-only"> Increased by
                            </span>
                            0
                        </div>
                    </dd>
                </div>
                <div class="px-4 py-5 sm:p-6">
                    <dt class="text-base font-normal text-gray-900">
                        Product Name
                    </dt>
                    <dd class="flex items-baseline justify-between mt-1 md:block lg:flex">
                        <div class="flex items-baseline text-2xl font-semibold text-primary-600">
                            Stats
                            <span class="ml-2 text-sm font-medium text-gray-500">from 0</span>
                        </div>

                        <div class="inline-flex items-baseline px-2.5 py-0.5 rounded-full text-sm font-medium md:mt-2 lg:mt-0">
                            <ArrowUpIcon class="-ml-1 mr-0.5 h-5 w-5 flex-shrink-0 self-center text-green-500"
                                aria-hidden="true" />
                            <ArrowDownIcon class="-ml-1 mr-0.5 h-5 w-5 flex-shrink-0 self-center text-red-500"
                                aria-hidden="true" />
                            <span class="sr-only"> Increased by
                            </span>
                            0
                        </div>
                    </dd>
                </div>
                <div class="px-4 py-5 sm:p-6">
                    <dt class="text-base font-normal text-gray-900">
                        Product Name
                    </dt>
                    <dd class="flex items-baseline justify-between mt-1 md:block lg:flex">
                        <div class="flex items-baseline text-2xl font-semibold text-primary-600">
                            Stats
                            <span class="ml-2 text-sm font-medium text-gray-500">from 0</span>
                        </div>

                        <div class="inline-flex items-baseline px-2.5 py-0.5 rounded-full text-sm font-medium md:mt-2 lg:mt-0">
                            <ArrowUpIcon class="-ml-1 mr-0.5 h-5 w-5 flex-shrink-0 self-center text-green-500"
                                aria-hidden="true" />
                            <ArrowDownIcon class="-ml-1 mr-0.5 h-5 w-5 flex-shrink-0 self-center text-red-500"
                                aria-hidden="true" />
                            <span class="sr-only"> Increased by
                            </span>
                            0
                        </div>
                    </dd>
                </div>
            </dl>

            <h2 class="my-5 text-lg font-medium leading-6 text-gray-900">
                Recent activity
            </h2>
            <div class="hidden sm:block">
                <div class="flex flex-col ">
                    <div class="min-w-full overflow-hidden overflow-x-auto align-middle shadow sm:rounded-lg">
                        <table class="min-w-full divide-y divide-gray-200">
                            <thead>
                                <tr>
                                    <th class="px-6 py-3 text-sm font-semibold text-left text-gray-900 bg-gray-50" scope="col">
                                        Transaction
                                    </th>
                                    <th class="px-6 py-3 text-sm font-semibold text-right text-gray-900 bg-gray-50" scope="col">
                                        Amount
                                    </th>
                                    <th class="hidden px-6 py-3 text-sm font-semibold text-left text-gray-900 bg-gray-50 md:block"
                                        scope="col">
                                        Status
                                    </th>
                                    <th class="px-6 py-3 text-sm font-semibold text-right text-gray-900 bg-gray-50" scope="col">
                                        Date
                                    </th>
                                </tr>
                            </thead>
                            <tbody class="bg-white divide-y divide-gray-200">
                                <tr class="bg-white">
                                    <td class="w-full px-6 py-4 text-sm text-gray-900 max-w-0 whitespace-nowrap">
                                        <div class="flex">
                                            <a href="#"
                                                class="inline-flex space-x-2 text-sm truncate group">
                                                <ShoppingCartIcon
                                                    class="flex-shrink-0 w-5 h-5 text-gray-400 group-hover:text-gray-500"
                                                    aria-hidden="true" />
                                                <p class="text-gray-500 truncate group-hover:text-gray-900">Admin User</p>
                                            </a>
                                        </div>
                                    </td>
                                    <td class="px-6 py-4 text-sm text-right text-gray-500 whitespace-nowrap">
                                        <span class="font-medium text-gray-900">100.00</span>
                                        PHP
                                    </td>
                                    <td class="hidden px-6 py-4 text-sm text-gray-500 whitespace-nowrap md:block">
                                        <span
                                            class="inline-flex items-center px-2.5 py-0.5 rounded-full text-xs font-medium capitalize bg-yellow-100">Pending</span>
                                    </td>
                                    <td class="px-6 py-4 text-sm text-right text-gray-500 whitespace-nowrap">
                                        Feb 14, 2023 - 02:31 AM
                                    </td>
                                </tr>
                                <tr class="bg-white">
                                    <td class="w-full px-6 py-4 text-sm text-gray-900 max-w-0 whitespace-nowrap">
                                        <div class="flex">
                                            <a href="#"
                                                class="inline-flex space-x-2 text-sm truncate group">
                                                <ShoppingCartIcon
                                                    class="flex-shrink-0 w-5 h-5 text-gray-400 group-hover:text-gray-500"
                                                    aria-hidden="true" />
                                                <p class="text-gray-500 truncate group-hover:text-gray-900">Mang Jose</p>
                                            </a>
                                        </div>
                                    </td>
                                    <td class="px-6 py-4 text-sm text-right text-gray-500 whitespace-nowrap">
                                        <span class="font-medium text-gray-900">1000.00</span>
                                        PHP
                                    </td>
                                    <td class="hidden px-6 py-4 text-sm text-gray-500 whitespace-nowrap md:block">
                                        <span
                                            class="inline-flex items-center px-2.5 py-0.5 rounded-full text-xs font-medium capitalize bg-green-100">Delivered</span>
                                    </td>
                                    <td class="px-6 py-4 text-sm text-right text-gray-500 whitespace-nowrap">
                                        Feb 14, 2023 - 02:31 AM
                                    </td>
                                </tr>
                            </tbody>
                        </table>
                    </div>
                </div>
            </div>
        </div>
    </AdminLayout>
</template>
