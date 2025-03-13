<script setup lang="ts">
import AppLayout from '@/layouts/AppLayout.vue';
import { type BreadcrumbItem } from '@/types';
import { Head } from '@inertiajs/vue3';
import SampleData from '@/components/statistics/SampleData.vue';
import AreaChart from '@/components/statistics/AreaChart.vue';
import PieChart from '@/components/statistics/PieChart.vue';
import BarChart from '@/components/statistics/BarChart.vue';

const breadcrumbs: BreadcrumbItem[] = [
    {
        title: 'Dashboard',
        href: '/dashboard',
    },
];
</script>

<template>

    <Head title="Dashboard" />

    <AppLayout :breadcrumbs="breadcrumbs">
        <div class="flex h-full flex-1 flex-col gap-4 rounded-xl p-4">
            <!-- Grid for charts with equal heights -->
            <div class="grid grid-rows-2 md:grid-cols-3 md:grid-rows-1 gap-4">
                <!-- PieChart -->
                <div
                    class="relative overflow-hidden rounded-xl border border-sidebar-border/70 dark:border-sidebar-border flex">

                    <PieChart class="w-full h-full" />

                </div>
                <!-- AreaChart -->
                <div
                    class="relative overflow-hidden rounded-xl border border-sidebar-border/70 dark:border-sidebar-border flex">

                    <AreaChart class="w-full h-full" />

                </div>
                <!-- SampleData -->
                <div
                    class="relative overflow-hidden rounded-xl border border-sidebar-border/70 dark:border-sidebar-border flex">

                    <SampleData class="w-full h-full" />

                </div>
            </div>
            <!-- BarChart -->
            <div class="relative flex-1 rounded-xl border border-sidebar-border/70 dark:border-sidebar-border flex">

                <BarChart class="w-full h-full" />

            </div>
        </div>
    </AppLayout>

</template>
