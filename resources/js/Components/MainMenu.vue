<script setup>
import { Squares2X2Icon } from '@heroicons/vue/24/outline'
import { UsersIcon } from '@heroicons/vue/24/outline'

import SideLink from '@/Components/SideLink.vue';
</script>

<template>
    <div class="px-2 pb-6 border-b border-primary-600">
        <div class="mb-2">
            <SideLink :href="route('dashboard')" :active="route().current('dashboard')">
                <Squares2X2Icon class="h-5 w-5 mr-4" />
                Dashboard
            </SideLink>
        </div>
    </div>

    <div class="px-2 pt-6">
        <div class="mb-2">
            <SideLink :href="route('profile.edit')" :active="route().current('profile.*')">
                <UsersIcon class="h-5 w-5 mr-4" />
                User Profile
            </SideLink>
        </div>

        <footer class="absolute inset-x-0 bottom-0 cursor-pointer ">
            <div class="px-4 py-4 pb-3">
                <div class="text-xs font-medium text-white">
                    All rights reserved
                    © 2023-2024
                </div>
                <div class="flex items-center space-x-2 text-xs text-primary-300">
                    <span>
                        App version 0.0.1
                    </span>
                </div>
            </div>
        </footer>
    </div>
</template>
