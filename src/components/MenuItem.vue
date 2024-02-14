<script setup lang="ts">
    import { RouterLink } from 'vue-router';
    import type { IMenuItem } from '@/interfaces/IMenuItems';
    defineProps<{data: IMenuItem}>()
</script>

<template>
    <RouterLink class="item" :to="data.path" :name="data.name">{{ data.name }}</RouterLink>
</template>

<style>
    .item{
        height: 100%;
        padding-top: 1rem;
        padding-bottom: 1rem;
        font-size: 1rem;
        
    }
</style>
