<script setup lang="ts">
import ApplicationLogo from "@/components/ApplicationLogo.vue"
</script>

<template>
    <footer
        class="bg-secondary text-primary-content py-3 px-6 text-sm flex flex-wrap items-center justify-between w-full">
        <!-- Left Section: Logo & Name -->
        <div class="flex items-center gap-2 ml-10">
            <div class="flex items-center">
                <ApplicationLogo class="w-10" />
            </div>
            <div class="flex flex-col leading-none">
                <h1 class="text-base font-semibold">PPD - RICTMS</h1>
                <p class="text-xs opacity-75">
                    Providing reliable solutions since 2025
                </p>
            </div>
        </div>

        <!-- Center: Copyright -->
        <p class="text-xs opacity-75 text-center">
            © 2025 - All rights reserved
        </p>

        <!-- Right: Social Media Links -->
        <div class="flex gap-3">
            <a href="https://fo4a.dswd.gov.ph/" target="_blank"
                class="border border-white rounded-full p-2 flex items-center justify-center w-8 h-8 hover:bg-white hover:text-primary transition">
                <i class="fa-solid fa-globe"></i>
            </a>

            <a href="https://web.facebook.com/dswdserves" target="_blank"
                class="border border-white rounded-full p-2 flex items-center justify-center w-8 h-8 hover:bg-white hover:text-primary transition">
                <i class="fa-brands fa-facebook-f"></i>
            </a>
        </div>
    </footer>
</template>
