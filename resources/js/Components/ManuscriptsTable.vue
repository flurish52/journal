<template>
    <div class="relative overflow-x-auto shadow-md sm:rounded-lg">
        <div class="flex flex-column sm:flex-row flex-wrap space-y-4 sm:space-y-0 items-center justify-between pb-4">
            <div class="relative">
                <div class="absolute inset-y-0 left-0 rtl:inset-r-0 rtl:right-0 flex items-center ps-3 pointer-events-none">
                    <svg class="w-5 h-5 text-gray-500 dark:text-gray-400" aria-hidden="true" fill="currentColor" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><path fill-rule="evenodd" d="M8 4a4 4 0 100 8 4 4 0 000-8zM2 8a6 6 0 1110.89 3.476l4.817 4.817a1 1 0 01-1.414 1.414l-4.816-4.816A6 6 0 012 8z" clip-rule="evenodd"></path></svg>
                </div>
                <SearchButton
                    :items="items"
                   class="block p-2 ps-10 text-sm text-gray-900 border border-gray-300 rounded-lg w-80 bg-gray-50 focus:ring-blue-500 focus:border-blue-500 dark:bg-gray-700 dark:border-gray-600 dark:placeholder-gray-400 dark:text-white dark:focus:ring-blue-500 dark:focus:border-blue-500" placeholder="Search for items"
                />
            </div>
        </div>

        <table class="w-full text-sm text-left rtl:text-right text-gray-500 dark:text-gray-400">
            <thead class="text-xs text-gray-700 uppercase bg-gray-50 dark:bg-gray-700 dark:text-gray-400">
            <tr>
<!--                <th scope="col" class="p-4">-->
<!--                    <div class="flex items-center">-->
<!--                        <input id="checkbox-all-search" type="checkbox" class="w-4 h-4 text-blue-600 bg-gray-100 border-gray-300 rounded-sm focus:ring-blue-500 dark:focus:ring-blue-600 dark:ring-offset-gray-800 dark:focus:ring-offset-gray-800 focus:ring-2 dark:bg-gray-700 dark:border-gray-600">-->
<!--                        <label for="checkbox-all-search" class="sr-only">checkbox</label>-->
<!--                    </div>-->
<!--                </th>-->
                <th scope="col" class="px-6 py-3">
                   Title
                </th>
                <th scope="col" class="px-6 py-3">
                    Abstract
                </th>
                <th scope="col" class="px-6 py-3">
                    keywords
                </th>
                <th scope="col" class="px-6 py-3">
                    Article type
                </th>
                <th scope="col" class="px-6 py-3">
                    Status
                </th>
                <th scope="col" class="px-6 py-3">
                    Submitted on
                </th>
                <th scope="col" class="px-6 py-3">
                    Download
                </th>
                <th scope="col" class="px-6 py-3">
                    Actions
                </th>
            </tr>
            </thead>
            <tbody>
            <tr
                v-for="item in items"
                class="bg-white border-b dark:bg-gray-800 dark:border-gray-700 border-gray-200 hover:bg-gray-50 dark:hover:bg-gray-600">
<!--                <td class="w-4 p-4">-->
<!--                    <div class="flex items-center">-->
<!--                        <input id="checkbox-table-search-1" type="checkbox" class="w-4 h-4 text-blue-600 bg-gray-100 border-gray-300 rounded-sm focus:ring-blue-500 dark:focus:ring-blue-600 dark:ring-offset-gray-800 dark:focus:ring-offset-gray-800 focus:ring-2 dark:bg-gray-700 dark:border-gray-600">-->
<!--                        <label for="checkbox-table-search-1" class="sr-only">checkbox</label>-->
<!--                    </div>-->
<!--                </td>-->
                <th scope="row" class="px-6 py-4 font-medium text-gray-900 whitespace-nowrap dark:text-white">
                    {{item.title}}
                </th>
                <td class="px-6 py-4">
                    {{ item.keywords.length > 30 ? item.keywords.slice(0, 100) + '...' : item.keywords }}
                </td>
                <td class="px-6 py-4">
                    {{ item.keywords }}
                </td>
                <td class="px-6 py-4">
                    {{item.article_type}}
                </td>
                <td class="px-6 py-4">
                    under review <br>
<!--                    Editor's comment-->
                </td>
                <td class="px-6 py-4">
                    {{ new Date(item.created_at).toLocaleDateString() }}
                    <br>
<!--                    Editor's comment-->
<!--                    Viewer's feedback-->
                </td>
                <td class="px-6 py-4">
                    <a href="#" class="font-medium text-blue-600 dark:text-blue-500 hover:underline">Download</a>
                </td>
                <td class="px-6 py-4">
                    <Link href="#" class="font-medium text-blue-600 dark:text-blue-500 hover:underline">Delete</Link>
                    <br>
                    <Link href="#" class="font-medium text-blue-600 dark:text-blue-500 hover:underline">View</Link>
                </td>

            </tr>
            </tbody>
        </table>
    </div>
</template>

<script setup>
import {Link} from "@inertiajs/vue3";
import SearchButton from "@/Components/SearchButton.vue";

defineProps({
    items:Array
})
</script>

<style scoped>

</style>
