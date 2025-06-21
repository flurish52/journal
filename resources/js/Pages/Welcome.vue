<template>
    <GuestLayout>
        <div
            class="flex min-h-screen flex-col items-center bg-gray-100 pt-6 sm:justify-center sm:pt-0"
        >
            <h1 class="flex items-center justify-center gap-4 p-4 bg-white shadow-md rounded-xl">
                <Link href="/" class="py-2 px-4 text-gray-800 hover:text-blue-600 transition-colors duration-300">
        <span class="text-2xl md:text-3xl font-extrabold text-center text-gray-900">
            Welcome to the National Association for Exceptional Children
        </span>
                </Link>
            </h1>


            <!-- Article Section Start -->
            <section class="w-full max-w-7xl py-10">
                <h3 class="text-3xl font-semibold text-center mb-8">Latest Articles</h3>
                <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-6">
                    <div
                        v-for="article in articles"
                        :key="article.id"
                        class="bg-white shadow-md rounded-lg overflow-hidden hover:shadow-lg transition"
                    >
                        <img
                            :src="article.image"
                            alt="Article image"
                            class="w-full h-48 object-cover"
                        />
                        <div class="p-4">
                            <h3 class="text-xl font-bold text-gray-800 mb-2">
                                {{ article.title }}
                            </h3>
                            <p class="text-gray-600 text-sm">
                                {{ article.summary }}
                            </p>
                            <Link
                                :href="`/articles/${article.id}`"
                                class="inline-block mt-4 text-blue-600 hover:underline font-medium"
                            >
                                Read More
                            </Link>
                        </div>
                    </div>
                </div>
            </section>
            <!-- Article Section End -->


            <!-- Explore More Articles Button -->
            <div class="text-center mt-10">
                <Link
                    href="/articles"
                    class="bg-blue-600 text-white px-6 py-3 rounded-md shadow-md hover:bg-blue-700 transition"
                >
                    Explore More Articles
                </Link>
            </div>
            <!-- Explore More Articles Button -->

        </div>
    </GuestLayout>

</template>

<script setup>
import {Link} from "@inertiajs/vue3";
import Footer from "@/Components/Footer.vue";
import GuestLayout from "@/Layouts/GuestLayout.vue";

const articles = [
    {
        id: 1,
        title: "Supporting Inclusive Education",
        summary: "Learn how inclusive education benefits all learners and how schools can implement it effectively.",
        image: "Inclusive.jpeg"
    },
    {
        id: 2,
        title: "Empowering Exceptional Children",
        summary: "This article explores different strategies for empowering children with special needs.",
        image: "Empowering.jpeg"
    },
    {
        id: 3,
        title: "Building Strong Communities",
        summary: "Strong community support can greatly improve outcomes for exceptional children.",
        image: "strong.jpeg"
    }
]
</script>
