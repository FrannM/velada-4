<template>
  <nav class="bg-transparent">
    <div class="mx-auto max-w-max px-2 sm:px-6 lg:px-8">
      <div class="flex justify-around items-center h-16">

        <!-- Sección izquierda -->
        <div class="flex">
          <a v-for="item in navigation.slice(0, 2)" :key="item.name" :href="item.href"
             :class="[item.current ? 'text-white hover:text-white px-10 py-10 rounded-md text-lg font-medium' : 'text-gray-300 hover:text-white px-10 py-10 rounded-md text-lg font-medium']"
             :aria-current="item.current ? 'page' : undefined">{{ item.name }}</a>
        </div>

        <!-- Sección central: Logo o Imagen -->
        <div class="flex-grow text-center">
          <HeroLogo/>
        </div>

        <!-- Sección derecha -->
        <div class="flex">
          <a v-for="item in navigation.slice(2)" :key="item.name" :href="item.href"
             :class="[item.current ? 'text-white hover:text-white px-10 py-10 rounded-md text-lg font-medium' : 'text-gray-300 hover:text-white px-10 py-10 rounded-md text-lg font-medium']"
             :aria-current="item.current ? 'page' : undefined">{{ item.name }}</a>
        </div>

      </div>
    </div>
  </nav>
</template>

<script setup lang="ts">
import {ref} from 'vue';
import HeroLogo from "@/components/HeroLogo.vue";

const navigation = ref([
  {name: 'Evento', href: '#', current: true},
  {name: 'Combate', href: '#', current: false},
  {name: 'Pronósticos', href: '#', current: false},
  {name: 'Entradas', href: '#', current: false},
]);
</script>

<style>
/* Estilos adicionales si son necesarios */
</style>
