<template>
    <div class="relative overflow-x-auto shadow-md sm:rounded-lg">
        <h1 class="text-3xl text-center underline font-bold text-gray-800">All Papers</h1>
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

<div>
    <h2 class="text-2xl underline text-center font-semibold text-gray-700 mt-6">Published papers</h2>
    <PublishedPapers
    :items="items"
    />
</div>
        <div>
    <h2 class="text-2xl underline text-center font-semibold text-gray-700 mt-6">Accepted</h2>

    <AcceptedPapers
    :items="items"
    />
</div>

        <div>
            <h2 class="text-2xl underline text-center font-semibold text-red-700 mt-6">Rejected papers</h2>
        <RejectedPapers
    :items="items"
    />
        </div>

        <div>
            <h2 class="text-2xl underline text-center font-semibold text-red-700 mt-6">Papers Under Review</h2>
        <UnderReview
    :items="items"
    />
        </div>

    </div>
</template>

<script setup>

import SearchButton from "@/Components/SearchButton.vue";
import AcceptedPapers from "@/Components/AcceptedPapers.vue";
import RejectedPapers from "@/Components/RejectedPapers.vue";
import UnderReview from "@/Components/UnderReview.vue";
import PublishedPapers from "@/Components/PublishedPapers.vue";
defineProps({
    items:Array
})
</script>

<style scoped>

</style>
