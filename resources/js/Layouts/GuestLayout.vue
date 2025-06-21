<script setup>
import NavBar from "@/Components/NavBar.vue";
import Footer from "@/Components/Footer.vue";

</script>

<template>
    <div class="px-6 lg:px-12 bg-gray-50 relative">

        <NavBar />
        <div
            class="flex min-h-screen flex-col items-center bg-gray-100 pt-6 sm:justify-center sm:pt-0"
        >
                <slot />

        <Footer />
    </div>
    </div>
</template>

