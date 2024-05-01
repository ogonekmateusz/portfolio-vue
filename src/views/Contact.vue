<template>
    <section class="contact">
        <div class="container col-xxl-10 py-5">
            <div class="row d-flex">
                <div class="col-lg-6 my-3">
                    <div class="services-header">
                        <h2>Czekamy na Twoje pytania!</h2>
                    </div>
                    <div class="services-header">
                        <div class="services-header-content">
                            <hr class="line"> <span>Skontaktuj się z nami już dziś!</span> 
                        </div>
                        <div class="services-description">
                            <p>Prześlij nam szczegóły dotyczące Twojego projektu, takie jak oczekiwania, funkcjonalności, terminy i budżet, abyśmy mogli przygotować ofertę i omówić współpracę.</p>
                        </div>
                    </div>
                </div>
                <div class="col-lg-6">
                    <form class="d-flex flex-column align-items-center emailForm"  method="POST" action="https://formspree.io/f/mpzvbron">
                        <div class="form-group py-4 w-100"> 
                            <input type="text" class="form-control input" placeholder="Imię i Nazwisko" name="imieINazwisko">
                        </div>
                        <div class="form-group py-2 w-100"> 
                            <input type="email" class="form-control input" placeholder="Adres Email" name="mail">
                        </div>
                        <div class="form-group py-4 w-100"> 
                            <input type="tel" class="form-control input" placeholder="Numer Telefonu"  name="NumerTelefonu">
                        </div>
                        <div class="form-group w-100"> 
                            <textarea class="form-control" name="msg" placeholder="Opis"></textarea>
                        </div>         
                        
                            <button type="submit" class="my-5 btn btn-primary">Zatwierdź</button>                  
                    </form>
                </div>
            </div>
        </div>
    </section>
</template>

<script setup lang="ts">
import 'bootstrap/dist/css/bootstrap.css';
import 'bootstrap/dist/js/bootstrap.bundle';
</script>

<style scoped>
@import url(/src/assets/colors.css);

.contact {
    margin-top: 6rem;
}

.form-control {
    border: none;
    background-color: transparent;
    color: var(--white);
    border-bottom: 3px solid var(--primary);
    border-radius: 0;
    font-weight: bold;
}

.form-control::placeholder {
    color: var(--white);
}

.contact .form-control:focus {
    box-shadow: none !important;
}

.btn {
   background: transparent;
   color: white;
   border-radius: 0;
   font-size: 1.1rem;
   font-weight: bold;
   border: 1px solid var(--primary);
   transition: .3s ease-in-out;
   padding: 0.7rem 1.4rem;
}

.btn:hover {
    background-color: var(--primary) !important;
     border-color: var(--dark) !important;
     color: black !important;
}


</style>
