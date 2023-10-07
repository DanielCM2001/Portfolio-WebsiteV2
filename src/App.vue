<template>
  <main>
    <TheNavBarVue />
    <RouterView />
  </main>
</template>

<script setup>
import { RouterView } from "vue-router";
import TheNavBarVue from "./components/TheNavBar.vue";
</script>
