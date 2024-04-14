<template>
    <section>
      <h2>7+ years experience working</h2>
      <section class="cardServices">
        <div class="box">
            <img :src="require('@/assets/icon-1.png')" alt="img">
            <h3>{{ title }}</h3>
            <p>{{ description }}</p>
        </div>
      </section>
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

    section {
        padding: 80px 100px;
    }
  
    h2 {
        color: var(--white);
        font-weight: bold;
        font-size: 46px;
        line-height: 56px;
    }

    .box {
        margin: 46px;
        background-color:var(--lightDark) ;
        padding: 68px 25px;
    }

    .box h3 {
        line-height: 32px;
        font-size: 26px;
        font-weight: bold;
        color: var(--white);
        margin: 18px 0;
    }
    .box p {
        font-size: 16px;
        line-height: auto;
        color: var(--gray);
    }
  </style>
  