<script setup lang="ts"> 
    import router from '@/router';
    import MenuItem from './MenuItem.vue';
    import type { IMenuItem } from '@/interfaces/IMenuItems';
    const links = router.options.routes.filter((item)=>{
        return {
            name: item.name,
            path: item.path
        }
    }) as IMenuItem[]
</script>

<template>
    <nav>
        <MenuItem class="nav-item" v-for="items in links" :data="items" :name="items.name" :path="items.path" :key="items.name"></MenuItem>
    </nav>
</template>

<style>
    nav{
        width: 100%;
        display: flex;
        align-items: center;
        justify-content: space-between;
    }
    .nav-item{
        width: 100%;
        text-align: center;
    }
</style>