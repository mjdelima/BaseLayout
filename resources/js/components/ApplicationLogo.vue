<script setup lang="ts">
import { ref } from "vue";
import { Link } from "@inertiajs/vue3";

// Define reactive data
const imagePath = ref("/img/dswd.png");
</script>

<template>
    <Link :href="'/'">
    <img :src="imagePath" class="size-16 object-contain" alt="DSWD Logo" />
    </Link>
</template>
