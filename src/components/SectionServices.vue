<template>
    <section>
      <h2>7+ years experience working</h2>
      <div class="box">
        <img :src="require('@/assets/icon-1.png')" alt="img">
        <h3>{{ title }}</h3>
        <p>{{ description }}</p>
      </div>
    </section>
  </template>
  
  <script lang="ts" setup>
  defineProps<{
    title: string,
    imgSrc: string,
    description: string
  }>()
  </script>
  
  <style scoped>
  /* Dodaj style jeśli potrzebujesz */
  </style>
  