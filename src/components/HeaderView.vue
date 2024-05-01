<template>
  <nav class="navbar navbar-expand-md navbar-dark bg-dark p-3" aria-label="Fourth navbar example">
    <div class="container-fluid">
      <RouterLink to="/" class="navbar-brand">CodeCarrot<span>.</span> </RouterLink>
      <!-- <a class="navbar-brand" href="#">CodeCarrot<span>.</span> </a> -->
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarsExample04" aria-controls="navbarsExample04" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>

      <div class="collapse navbar-collapse" id="navbarsExample04">
        <ul class="navbar-nav ms-auto mb-2 mb-md-0">
          <li class="nav-item">
            <RouterLink class="nav-link" to="/">Strona Główna</RouterLink>
          </li>
          <li class="nav-item">
            <RouterLink class="nav-link" to="/">Co oferujemy</RouterLink>
          </li>
          <li class="nav-item">
            <RouterLink class="nav-link" to="/">Nasze projekty</RouterLink>
          </li>
          <li class="nav-item">
            <RouterLink class="nav-link" to="/">o nas</RouterLink>
          </li>
          <li class="nav-item border ">
            <RouterLink class="nav-link last" to="/Contact">Kontakt</RouterLink>
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

@import url(/src/assets/colors.css);
/* Styl dla nawigacji */
.navbar {
  background-color: var(--dark) !important; /* Ustawienie koloru tła paska nawigacji */
  font-weight: bold;
  width: 100%;
  position: fixed;
  left: 0; 
  top: 0; 
  z-index: 1000;
}

/* Styl dla marki */
.navbar-brand {
  font-size: 24px;
  color: var(--white); /* Kolor tekstu marki */
  line-height: 28px;
}

.navbar-brand span {
  color: var(--primary); /* Kolor dodatkowego punktu w marki */
}

/* Styl dla linków nawigacyjnych */
.nav-link {
  position: relative;
  color: var(--white); /* Kolor tekstu linków */
  text-decoration: none;
  font-size: 14px;
  line-height: auto;
  font-weight: bold;
  transition: color 0.3s ease-in-out; /* Animacja zmiany koloru */
  margin: 0 12px;
}

/* Styl dla ostatniego elementu nawigacji */
.nav-item:last-child {
  border-color: var(--primary) !important; /* Kolor obramowania ostatniego elementu */
  margin-left: 20px;
  transition: .3s ease-in-out;
  cursor: pointer;
}

/* Styl dla pozostałych elementów nawigacji */
.nav-item {
  position: relative;
}

/* Animacja dla elementów nawigacyjnych */
.nav-item::after {
  content: "";
  position: absolute;
  bottom: -2px;
  left: 0;
  width: 0%;
  height: 2px;
  background-color: var(--primary);
  transform-origin: right;
  transition: width 0.35s ease-in-out;
}

/* Animacja dla elementów nawigacyjnych po najechaniu myszką */
.nav-item:not(:last-child):hover::after {
  width: 100%;
}

/* Styl dla ostatniego elementu nawigacji po najechaniu myszką */
.nav-item:last-child:hover {
  background-color: var(--primary) !important;
  border-color: var(--dark) !important;
}

.last:hover {
  color: black !important;
}

/* Media queries dla ekranów o szerokości do 768px */
@media (max-width: 768px) {

.nav-item {
  padding: 5px 0;
}

.nav-link {
  margin: 0;
}

.nav-item::after {
  background-color: transparent;
  left: 10px;
}

.nav-item:not(:last-child):hover::after {
  width: 29%;
}

.nav-item:last-child {
  margin: 0;
  border: none !important;
}

.last:hover {
  color: var(--white) !important; 
}

.navbar-nav > .nav-item:last-child:hover {
  background-color: transparent !important; 
  border-color: transparent !important; 
  color: var(--white) !important;
}

.navbar-nav > .nav-item:last-child:hover::after {
  width: 0; 
}

.last::after, .nav-item::after {
  content: "";
  position: absolute;
  bottom: -2px;
  left: 0;
  width: 0%;
  height: 2px;
  background-color: var(--primary);
  transform-origin: right;
  transition: width 0.35s ease-in-out;
}

.last:hover::after {
  width: 15%;
}
}


</style>
