<template>
    <header>
        <h2>Alifreza<span>.</span></h2>
        <nav>
            <RouterLink to="/">Home</RouterLink>
            <RouterLink to="/">Services</RouterLink>
            <RouterLink to="/">Work</RouterLink>
            <RouterLink to="/">About us</RouterLink>
            <RouterLink to="/">Blog</RouterLink>
            <RouterLink to="/">Contact</RouterLink>
        </nav>
    </header>
</template>
  
<script lang="ts" setup>
import { RouterLink } from 'vue-router'; 
</script>
  
<style scoped>

header {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: space-between;
  z-index: 1000;
  background-color: var(--dark);
}

h2 {
  color: var(--white);
  font-size: 24px;
  line-height: 28px;
  font-weight: bold;
  margin-left: 123px;
}

nav {
  margin-right: 123px;
}

a {
  position: relative;
  color: var(--white);
  text-decoration: none;
  font-size: 14px;
  line-height: auto;
  font-weight: bold;
  padding: 10px 15px;
  transition: color 0.3s ease-in-out;
  margin: 0 5px;
}

a:not(:last-child)::after{
  content: "";
  position: absolute;
  bottom: -2px;
  left: 0;
  width: 0%;
  height: 2px;
  background-color: var(--primary);
  transform-origin: right;
  transition: width 0.3s ease-in-out;
}

a:not(:last-child):hover::after{
  width: 100%;
}

nav a:last-child {
  border: 1px solid var(--primary);
  margin-left: 20px;
}

nav a:last-child:hover {
  background-color: var(--primary);
  border-color: var(--dark);
  color: var(--dark);
}

span {
  color: var(--primary);
}
</style>
  