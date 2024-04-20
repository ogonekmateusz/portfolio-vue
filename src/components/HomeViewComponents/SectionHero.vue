<template>
    <section>
      <h2>Hello, I'm Alif Reza</h2>
      <h1>Product Designer</h1>
      <p>I’m from Singapore and I have been working as a Product Designer for more than 7 years. I’ve worked for a Hanziree company Pabloo as a Product Designer and Front-end Developer for 3 years.</p>
      <EmailMe class="button"></EmailMe>
    </section>
  </template>
  
  <script lang="ts" setup>
  import EmailMe from "../EmailMe.vue";
  </script>
  
  <style scoped>
  section {
    margin-top: 80px;
    padding: 80px 100px;
    width: 50%;
  }
  
  h2 {
    color: var(--primary);
    font-size: 38px;
    font-weight: bold;
    margin: 0;
  }
  
  h1 {
    font-size: 88px;
    color: var(--white);
    margin: 0;
  }
  
  p {
    color: var(--gray);
    font-size: 16px;
    line-height: 28px;
    width: 60%;
  }
  
  
  </style>
  