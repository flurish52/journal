<template>
    <GuestLayout>
        <section class="bg-white text-gray-800 min-h-screen px-6 md:px-20 py-16">
            <!-- Header -->
            <div class="text-center mb-16">
                <h1 class="text-4xl md:text-5xl font-extrabold text-teal-700 mb-4">About Us</h1>
                <p class="text-lg md:text-xl text-gray-600 max-w-2xl mx-auto">We are passionate innovators, dreamers, and doers — committed to making a difference through exceptional service and creative excellence.</p>
            </div>

            <!-- Main Grid -->
            <div class="grid md:grid-cols-2 gap-12 items-center">
                <!-- Image -->
                <div>
                    <img src="https://source.unsplash.com/600x400/?team,office" alt="Our Team" class="rounded-2xl shadow-xl w-full object-cover">
                </div>

                <!-- Text Content -->
                <div>
                    <h2 class="text-2xl font-bold text-teal-600 mb-4">Who We Are</h2>
                    <p class="text-gray-700 mb-4 leading-relaxed">
                        Founded in 2017, our organization has grown from a small startup to a thriving community of passionate professionals. We believe in people, purpose, and progress — and we bring these values to everything we create.
                    </p>

                    <h2 class="text-2xl font-bold text-teal-600 mb-4 mt-10">Our Mission</h2>
                    <p class="text-gray-700 mb-4 leading-relaxed">
                        To empower businesses and individuals by delivering innovative solutions that make lives easier, better, and more fulfilling. We aim to build trust and long-lasting impact through technology, creativity, and care.
                    </p>

                    <h2 class="text-2xl font-bold text-teal-600 mb-4 mt-10">Our Vision</h2>
                    <p class="text-gray-700 mb-4 leading-relaxed">
                        To be a global leader in shaping the future by creating tools, platforms, and experiences that inspire growth, connection, and transformation.
                    </p>
                </div>
            </div>

            <!-- Core Values -->
            <div class="mt-20">
                <h2 class="text-3xl font-extrabold text-center text-teal-700 mb-8">Our Core Values</h2>
                <div class="grid sm:grid-cols-2 lg:grid-cols-4 gap-8">
                    <div class="bg-teal-50 p-6 rounded-xl shadow hover:shadow-lg transition">
                        <h3 class="text-xl font-semibold text-teal-700 mb-2">Integrity</h3>
                        <p class="text-gray-600">We uphold honesty and strong moral principles in every decision we make.</p>
                    </div>
                    <div class="bg-teal-50 p-6 rounded-xl shadow hover:shadow-lg transition">
                        <h3 class="text-xl font-semibold text-teal-700 mb-2">Innovation</h3>
                        <p class="text-gray-600">We embrace change, challenge norms, and seek bold, creative solutions.</p>
                    </div>
                    <div class="bg-teal-50 p-6 rounded-xl shadow hover:shadow-lg transition">
                        <h3 class="text-xl font-semibold text-teal-700 mb-2">Collaboration</h3>
                        <p class="text-gray-600">We grow together through teamwork, communication, and shared goals.</p>
                    </div>
                    <div class="bg-teal-50 p-6 rounded-xl shadow hover:shadow-lg transition">
                        <h3 class="text-xl font-semibold text-teal-700 mb-2">Excellence</h3>
                        <p class="text-gray-600">We go the extra mile to exceed expectations and deliver premium quality.</p>
                    </div>
                </div>
            </div>

            <!-- Call to Action -->
            <div class="mt-24 text-center">
                <h2 class="text-3xl font-bold text-gray-800 mb-4">Join Us on Our Journey</h2>
                <p class="text-gray-600 mb-6 max-w-2xl mx-auto">Whether you're a customer, partner, or aspiring team member, we welcome you to be part of our story.</p>
                <a href="/contact" class="inline-block bg-teal-700 text-white px-6 py-3 rounded-full font-semibold hover:bg-teal-800 transition">Contact Us</a>
            </div>
        </section>
    </GuestLayout>
</template>

<script setup>

import GuestLayout from "@/Layouts/GuestLayout.vue";
</script>
