<template>
   <HeaderView/>
  <router-view/>
  <SectionHero/>
</template>

<script setup lang="ts">
  import HeaderView from "./components/HeaderView.vue"
  import SectionHero from "./components/SectionHero.vue";
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@100..900&display=swap');
@import "@/assets/colors.css";
@import "@/assets/global.css";
</style>
