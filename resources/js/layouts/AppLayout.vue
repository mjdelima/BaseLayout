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
    <AppLayout :breadcrumbs="breadcrumbs">
        <slot />
        <footer>
            <FooterMenu />
        </footer>
    </AppLayout>
</template>
