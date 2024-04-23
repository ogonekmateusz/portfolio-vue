<template>
    <!-- <section>
      <h2>Hello, I'm Alif Reza</h2>
      <h1>Product Designer</h1>
      <p></p>
      <EmailMe class="button"></EmailMe>
    </section> -->

    <div class="container col-xl-10 col-xxl-8 px-4 py-5">
    <div class="row align-items-center g-lg-5 py-5">
      <div class="col-lg-7 text-center text-lg-start" >
        <div class="hello">Hello I'm Allif Reza</div>
        <h1 class="display-4 fw-bold lh-1 text-body-emphasis mb-3" >Product Designer</h1>
        <p class="col-lg-10 fs-4">I’m from Singapore and I have been working as a Product Designer for more than 7 years. I’ve worked for a Hanziree company Pabloo as a Product Designer and Front-end Developer for 3 years.</p>
        <EmailMe></EmailMe>
      </div>
      <div class="col-md-10 mx-auto col-lg-5">
        
      </div>
    </div>
  </div>
  </template>
  
<script lang="ts" setup>
import EmailMe from "../EmailMe.vue";
import 'bootstrap/dist/css/bootstrap.css';
import 'bootstrap/dist/js/bootstrap.bundle';
  
</script>
  
<style scoped>
.display-5{
  color: var(--white) !important;
}
.hello{
  color: var(--primary);
  font-size: 38px;
  font-weight: bold;
}
.display-4{
  color: white !important;
  font-weight: 800;
  font-size: 4.2rem;
}
.col-lg-10{
  color: var(--gray) !important;
  line-height: 28px !important;
}

.col-lg-10 {
  font-size: 1.2rem !important; 
}
</style>
