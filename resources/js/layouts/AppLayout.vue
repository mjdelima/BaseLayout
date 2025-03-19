<script setup lang="ts">
import AppLayout from '@/layouts/app/AppSidebarLayout.vue';
import FooterMenu from "@/components/Menus/Footer.vue";
import type { BreadcrumbItemType } from '@/types';

interface Props {
    breadcrumbs?: BreadcrumbItemType[];
}

withDefaults(defineProps<Props>(), {
    breadcrumbs: () => [],
});
</script>


<template>
    <div class="flex flex-col min-h-screen">
        <header>
            <slot name="header"></slot>
        </header>

        <main class="flex-1">
            <AppLayout :breadcrumbs="breadcrumbs">
                <slot />
            </AppLayout>
        </main>

        <footer class="mt-auto w-full">
            <FooterMenu />
        </footer>
    </div>
</template>
