<template>
  <nav class="navbar navbar-expand-md navbar-dark bg-dark p-3" aria-label="Fourth navbar example">
    <div class="container-fluid">
      <a class="navbar-brand" href="#">Alifreza<span>.</span> </a>
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarsExample04" aria-controls="navbarsExample04" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>

      <div class="collapse navbar-collapse" id="navbarsExample04">
        <ul class="navbar-nav ms-auto mb-2 mb-md-0">
          <li class="nav-item">
            <RouterLink class="nav-link" to="/">Home</RouterLink>
          </li>
          <li class="nav-item">
            <RouterLink class="nav-link" to="/">Services</RouterLink>
          </li>
          <li class="nav-item">
            <RouterLink class="nav-link" to="/">Work</RouterLink>
          </li>
          <li class="nav-item">
            <RouterLink class="nav-link" to="/">About us</RouterLink>
          </li>
          <li class="nav-item">
            <RouterLink class="nav-link " to="/">Blog</RouterLink>
          </li>
          <li class="nav-item ">
            <RouterLink class="nav-link" to="/">Contact</RouterLink>
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>
  
<script lang="ts" setup>
import 'bootstrap/dist/css/bootstrap.css';
import 'bootstrap/dist/js/bootstrap.bundle';
import { RouterLink } from 'vue-router'; 
</script>
  
<style scoped>
.navbar {
  background-color: var(--dark) !important;
  font-weight: bold;
  width: 100%;
  position: fixed;
  left: 0; 
  top: 0; 
}

.navbar-brand {
  font-size: 24px;
  color: var(--white);
  line-height: 28px;
}

.navbar-brand span {
  color: var(--primary);
}

.nav-link {
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

.nav-item {
  position: relative;
}

.nav-item::after {
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

.nav-item:hover::after {
  width: 100%;
}
</style>
