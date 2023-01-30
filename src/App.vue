<template>
  <div class="text-light text-light">
    <navbar></navbar>
    <RouterView />
  </div>
</template>

<script setup lang="ts">
import { RouterLink, RouterView } from "vue-router";
import Navbar from "./components/Navbar.vue";
</script>

<style scoped></style>
