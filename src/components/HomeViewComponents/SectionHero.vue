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
        <div class="hello">CodeCarrot Studio</div>
        <h1 class="display-4 fw-bold lh-1 text-body-emphasis mb-3" >FrontEnd Developers</h1>
        <p class="col-lg-10 fs-4">CodeCarrot Studio to inicjatywa dwóch uczniów technikum programistycznego. Tworzymy wysokiej jakości strony internetowe</p>
        <EmailMe></EmailMe>
      </div>
      <div class="col-md-10 mx-auto col-lg-5">
        <img src="@/assets/loho.png" alt="Logo">
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
.col-md-10{
  display: flex;
  justify-content: center;
}
img{
  width: 120%;
  height: 50vh;
}
@media (max-width: 986px) {
  .col-md-10{
    margin-top: 4rem;
  }
    img{
      width: 100%;
      height: 50vh;
    }
}
</style>
