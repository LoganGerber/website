<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router';
import PageHeader from '@/components/PageHeader.vue';
</script>

<template>
	<PageHeader />
	<RouterView />
</template>

<style>
@import "@/assets/base.css";
@import "@/assets/dualGrid.css";
</style>
