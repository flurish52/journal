<template>
        <table class="w-full text-sm text-left rtl:text-right text-gray-500 dark:text-gray-400">
            <thead class="text-xs text-gray-700 uppercase bg-gray-50 dark:bg-gray-700 dark:text-gray-400">
            <tr>
                <th scope="col" class="p-4">
                    <div class="flex items-center">
                        <input id="checkbox-all-search" type="checkbox" class="w-4 h-4 text-blue-600 bg-gray-100 border-gray-300 rounded-sm focus:ring-blue-500 dark:focus:ring-blue-600 dark:ring-offset-gray-800 dark:focus:ring-offset-gray-800 focus:ring-2 dark:bg-gray-700 dark:border-gray-600">
                        <label for="checkbox-all-search" class="sr-only">checkbox</label>
                    </div>
                </th>
                <th scope="col" class="px-6 py-3">
                    Title
                </th>
                <th scope="col" class="px-6 py-3">
                    Author(s)
                </th>
                <th scope="col" class="px-6 py-3">
                    Status
                </th>
                <th scope="col" class="px-6 py-3">
                    Reviewers Assigned
                </th>
                <th scope="col" class="px-6 py-3">
                    Actions
                </th>
            </tr>
            </thead>
            <tbody>
            <tr
                v-for="item in items"
                v-show="item.status === 'accept'"
                class="bg-white border-b dark:bg-gray-800 dark:border-gray-700 border-gray-200 hover:bg-gray-50 dark:hover:bg-gray-600">
                <td class="w-4 p-4">
                    <div class="flex items-center">
                        <input id="checkbox-table-search-1" type="checkbox" class="w-4 h-4 text-blue-600 bg-gray-100 border-gray-300 rounded-sm focus:ring-blue-500 dark:focus:ring-blue-600 dark:ring-offset-gray-800 dark:focus:ring-offset-gray-800 focus:ring-2 dark:bg-gray-700 dark:border-gray-600">
                        <label for="checkbox-table-search-1" class="sr-only">checkbox</label>
                    </div>
                </td>
                <th scope="row" class="px-6 py-4 font-medium text-gray-900 whitespace-nowrap dark:text-white">
                    {{item.title}}
                </th>
                <td class="px-6 py-4">
                    {{ item.author?.name || 'Unknown' }}
                </td>
                <td class="px-6 py-4">
                    under Review
                </td>
                <td class="px-6 py-4">
                    2 of 3
                </td>
                <td class="px-6 py-4">
                    <Link :href="`/editor/${item.id}/view`" class="font-medium text-blue-600 dark:text-blue-500 hover:underline">View</Link>
                    <br>
                    <br>
                    <a :href="`/editor/${item.id}/track-review`" class="font-medium text-blue-600 dark:text-blue-500 hover:underline">Track Review</a>
                </td>
            </tr>
            </tbody>
        </table>
</template>

<script setup>

import SearchButton from "@/Components/SearchButton.vue";
import {Link} from "@inertiajs/vue3";
defineProps({
    items:Array
})
</script>

<style scoped>

</style>
