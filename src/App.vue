<script setup lang="ts">
import { RouterView } from 'vue-router'
import MenuComponent from '@/components/NavMenu.vue'
</script>

<template>
  <main>
    <header>
      <MenuComponent></MenuComponent>
    </header>
    <RouterView/>
  </main>
</template>

<style>
  main{
    margin-top: 2rem;
    width: 100%;
  }
  header{
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    padding-inline: 3rem;
  }
</style>
