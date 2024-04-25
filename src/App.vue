<script setup lang="ts">
import {RouterLink, RouterView} from 'vue-router'
import HeaderComponent from "@/components/HeaderComponent.vue";
// import HelloWorld from './components/HelloWorld.vue'
</script>

<template>
    <div class="fixed -z-50 h-full w-full background-container"></div>
    <HeaderComponent/>
    <RouterView/>
</template>

<style>
.background-container {
  background: url("https://cdn.lavelada.dev/effects/background.webp");
  background-size: cover;
}
</style>
