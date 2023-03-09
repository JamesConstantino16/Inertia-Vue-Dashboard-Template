<script setup>
import AdminLayout from '@/Layouts/AdminLayout.vue';
import DeleteUserForm from './Partials/DeleteUserForm.vue';
import UpdatePasswordForm from './Partials/UpdatePasswordForm.vue';
import UpdateProfileInformationForm from './Partials/UpdateProfileInformationForm.vue';
import { Head } from '@inertiajs/vue3';

defineProps({
    mustVerifyEmail: Boolean,
    status: String,
});
</script>

<template>
    <Head title="Profile" />

    <AdminLayout>
        <template #header>
            <h2 class="font-semibold text-xl text-gray-800 leading-tight">Profile</h2>
        </template>

        <div class="max-w-7xl mx-auto sm:px-4 lg:px-6 space-y-6">
            <div class="p-2 sm:p-6 bg-white shadow sm:rounded-lg">
                <UpdateProfileInformationForm
                    :must-verify-email="mustVerifyEmail"
                    :status="status"
                    class="max-w-xl"
                />
            </div>

            <div class="p-2 sm:p-6 bg-white shadow sm:rounded-lg">
                <UpdatePasswordForm class="max-w-xl" />
            </div>

            <div class="p-2 sm:p-6 bg-white shadow sm:rounded-lg">
                <DeleteUserForm class="max-w-xl" />
            </div>
        </div>
    </AdminLayout>
</template>
