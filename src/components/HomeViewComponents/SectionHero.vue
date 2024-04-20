<template>
    <section>
      <h2>Hello, I'm Alif Reza</h2>
      <h1>Product Designer</h1>
      <p>I’m from Singapore and I have been working as a Product Designer for more than 7 years. I’ve worked for a Hanziree company Pabloo as a Product Designer and Front-end Developer for 3 years.</p>
      <button class="button">Email me</button>
    </section>
  </template>
  
  <script lang="ts" setup>
  import { RouterLink } from 'vue-router'; 
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
  
  .button {
    display: inline-block;
    padding: 18px 28px;
    color: #fff;
    font-size: 18px;
    transition: all 0.3s;
    position: relative;
    z-index: 1;
    cursor: pointer;
    font-weight: bold;
    border: none;
    border: 1px solid var(--primary);
  }
  
  .button:after {
    content: "";
    position: absolute;
    bottom: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: var(--primary);
    z-index: -2;
  }
  
  .button:before {
    content: "";
    position: absolute;
    bottom: 0;
    left: 0;
    width: 0%;
    height: 100%;
    background-color: var(--dark);
    transition: all 0.3s;
    z-index: -1;
  }
  
  .button:hover {
    color: var(--white);
  }
  
  .button:hover:before {
    width: 100%;
  }
  </style>
  