<template>
  <SectionHero/>
  <!-- sekcja services -->
  <section class="services ">
    <div class="container">
      <div class="row">
        <div class="col-lg-6">
          <div class="services-header">
            <h2>Celujemy <br>w przyszłość</h2>
          </div>
        </div>
        <div class="col-lg-6">
          <div class="services-header">
            <div class="services-header-content">
              <hr class="line"> <span>Co oferujemy</span> 
            </div>
            <div class="services-description">
              <p>Discover the best services I offer, designed to ensure the success of your project.</p>
            </div>
          </div>
        </div>
      </div>
    </div>
    <!-- cards -->
    <div class="row m-5">
      <sevicesBlock
          v-for="(service, index) in services"
          :key="index"
          :title="service.title"
          :imgSrc="service.imgSrc"
          :description="service.description"
        />
    </div>
    <!-- cards end -->
  </section>
  <!-- koniec sekcji services -->
<section class="work">
  
  <div class="album py-5 bg-body-tertiary">
    <div class="container container-work">
        <div class="row">
          <div class="col-lg-6">
            <div class="services-header">
              <div class="services-header-content">
                <hr class="line"> <span>Ostatnie prace</span> 
              </div>
              <h2>Kilka naszych ostatnich<br> projektów.</h2>
            </div>
          </div>

          <div class="col-lg-6">
            <div class="services-header">
            
              <div class="services-header-right-block">
                <button>Zobacz wszystkie projekty</button>
              </div>
            </div>
          </div>
        </div>
      </div>
    <div class="container-block">
        <SectionWork
          v-for="work in works"
          :key="work"
          :title="work.title"
          :imgSrc="work.imgSrc"
          :description="work.href"
        >
        </SectionWork>
        
      </div>
  </div>
</section>

<section id="contact">
    <div class="container container-contact ">
        <div class="row">
          <div class="col-lg-6">
            <div class="services-header">
              <div class="services-header-content">
                <hr class="line"> <span>Kontakt</span> 
              </div>
              <h2>Jesteś zainteresowany współpracą? </h2>
            </div>
          </div>

          <div class="col-lg-6">
            <div class="services-header">
            
              <div class="services-header-right-block">
                <EmailMe/>
              </div>
            </div>
          </div>
        </div>
      </div>
</section>
<section id="footer" class="align-items-center d-flex">\
  <!-- ikonki-- -->
  <svg xmlns="http://www.w3.org/2000/svg" class="d-none" fill="currentColor">
  <symbol id="bootstrap" viewBox="0 0 118 94">
    <path fill-rule="evenodd"  clip-rule="evenodd" d="M24.509 0c-6.733 0-11.715 5.893-11.492 12.284.214 6.14-.064 14.092-2.066 20.577C8.943 39.365 5.547 43.485 0 44.014v5.972c5.547.529 8.943 4.649 10.951 11.153 2.002 6.485 2.28 14.437 2.066 20.577C12.794 88.106 17.776 94 24.51 94H93.5c6.733 0 11.714-5.893 11.491-12.284-.214-6.14.064-14.092 2.066-20.577 2.009-6.504 5.396-10.624 10.943-11.153v-5.972c-5.547-.529-8.934-4.649-10.943-11.153-2.002-6.484-2.28-14.437-2.066-20.577C105.214 5.894 100.233 0 93.5 0H24.508zM80 57.863C80 66.663 73.436 72 62.543 72H44a2 2 0 01-2-2V24a2 2 0 012-2h18.437c9.083 0 15.044 4.92 15.044 12.474 0 5.302-4.01 10.049-9.119 10.88v.277C75.317 46.394 80 51.21 80 57.863zM60.521 28.34H49.948v14.934h8.905c6.884 0 10.68-2.772 10.68-7.727 0-4.643-3.264-7.207-9.012-7.207zM49.948 49.2v16.458H60.91c7.167 0 10.964-2.876 10.964-8.281 0-5.406-3.903-8.178-11.425-8.178H49.948z"></path>
  </symbol>
  <symbol id="facebook" viewBox="0 0 16 16">
    <path d="M16 8.049c0-4.446-3.582-8.05-8-8.05C3.58 0-.002 3.603-.002 8.05c0 4.017 2.926 7.347 6.75 7.951v-5.625h-2.03V8.05H6.75V6.275c0-2.017 1.195-3.131 3.022-3.131.876 0 1.791.157 1.791.157v1.98h-1.009c-.993 0-1.303.621-1.303 1.258v1.51h2.218l-.354 2.326H9.25V16c3.824-.604 6.75-3.934 6.75-7.951z"/>
  </symbol>
  <symbol id="instagram" viewBox="0 0 16 16">
      <path d="M8 0C5.829 0 5.556.01 4.703.048 3.85.088 3.269.222 2.76.42a3.917 3.917 0 0 0-1.417.923A3.927 3.927 0 0 0 .42 2.76C.222 3.268.087 3.85.048 4.7.01 5.555 0 5.827 0 8.001c0 2.172.01 2.444.048 3.297.04.852.174 1.433.372 1.942.205.526.478.972.923 1.417.444.445.89.719 1.416.923.51.198 1.09.333 1.942.372C5.555 15.99 5.827 16 8 16s2.444-.01 3.298-.048c.851-.04 1.434-.174 1.943-.372a3.916 3.916 0 0 0 1.416-.923c.445-.445.718-.891.923-1.417.197-.509.332-1.09.372-1.942C15.99 10.445 16 10.173 16 8s-.01-2.445-.048-3.299c-.04-.851-.175-1.433-.372-1.941a3.926 3.926 0 0 0-.923-1.417A3.911 3.911 0 0 0 13.24.42c-.51-.198-1.092-.333-1.943-.372C10.443.01 10.172 0 7.998 0h.003zm-.717 1.442h.718c2.136 0 2.389.007 3.232.046.78.035 1.204.166 1.486.275.373.145.64.319.92.599.28.28.453.546.598.92.11.281.24.705.275 1.485.039.843.047 1.096.047 3.231s-.008 2.389-.047 3.232c-.035.78-.166 1.203-.275 1.485a2.47 2.47 0 0 1-.599.919c-.28.28-.546.453-.92.598-.28.11-.704.24-1.485.276-.843.038-1.096.047-3.232.047s-2.39-.009-3.233-.047c-.78-.036-1.203-.166-1.485-.276a2.478 2.478 0 0 1-.92-.598 2.48 2.48 0 0 1-.6-.92c-.109-.281-.24-.705-.275-1.485-.038-.843-.046-1.096-.046-3.233 0-2.136.008-2.388.046-3.231.036-.78.166-1.204.276-1.486.145-.373.319-.64.599-.92.28-.28.546-.453.92-.598.282-.11.705-.24 1.485-.276.738-.034 1.024-.044 2.515-.045v.002zm4.988 1.328a.96.96 0 1 0 0 1.92.96.96 0 0 0 0-1.92zm-4.27 1.122a4.109 4.109 0 1 0 0 8.217 4.109 4.109 0 0 0 0-8.217zm0 1.441a2.667 2.667 0 1 1 0 5.334 2.667 2.667 0 0 1 0-5.334z"/>
  </symbol>
  <symbol id="twitter" viewBox="0 0 16 16">
    <path d="M5.026 15c6.038 0 9.341-5.003 9.341-9.334 0-.14 0-.282-.006-.422A6.685 6.685 0 0 0 16 3.542a6.658 6.658 0 0 1-1.889.518 3.301 3.301 0 0 0 1.447-1.817 6.533 6.533 0 0 1-2.087.793A3.286 3.286 0 0 0 7.875 6.03a9.325 9.325 0 0 1-6.767-3.429 3.289 3.289 0 0 0 1.018 4.382A3.323 3.323 0 0 1 .64 6.575v.045a3.288 3.288 0 0 0 2.632 3.218 3.203 3.203 0 0 1-.865.115 3.23 3.23 0 0 1-.614-.057 3.283 3.283 0 0 0 3.067 2.277A6.588 6.588 0 0 1 .78 13.58a6.32 6.32 0 0 1-.78-.045A9.344 9.344 0 0 0 5.026 15z"/>
  </symbol>
</svg>
<!-- ikonki-- -->
<div class="container">
  <hr>
<div class="row">
          <div class="col-lg-6">
            <div class="services-header footer-header">
              <p>Strona stworzona przez <a href="/">Michała Zająca</a> oraz <a href="/">Mateusza Ogonka</a></p>
            </div>
          </div>

          <div class="col-lg-6">
            <div class="services-header footer-header">
            
              <div class="services-header-right-block list-unstyled footer-header">
                <li class="ms-3"><a class="text-body-secondary" href="#"><svg class="bi" width="24" height="24"><use xlink:href="#twitter"/></svg></a></li>
                <li class="ms-3"><a class="text-body-secondary" href="#"><svg class="bi" width="24" height="24"><use xlink:href="#instagram"/></svg></a></li>
                <li class="ms-3"><a class="text-body-secondary" href="#"><svg class="bi" width="24" height="24"><use xlink:href="#facebook"/></svg></a></li>
              </div>
            </div>
          </div>
        </div>
      </div>
</section>
</template>

<script setup lang="ts">
import SectionHero from "../components/HomeViewComponents/SectionHero.vue";
import sevicesBlock from "@/components/servicesBlock.vue";

import SectionServices from "../components/HomeViewComponents/SectionServices.vue";
import SectionWork from "@/components/HomeViewComponents/SectionWork.vue";
import SectionContact from "@/components/HomeViewComponents/SectionContact.vue";
import EmailMe from "@/components/EmailMe.vue";

interface Service {
  title: string;
  imgSrc: string;
  description: string;
}

interface Work {
  title: string;
  imgSrc: string;
  href: string;
}

const services: Service[] = [
  {
    title: "Product Designer",
    imgSrc: "icon-1.png",
    description: "I offer innovative and attention-grabbing product design services. From initial ideation to implementation"
  },
  {
    title: "Frontend",
    imgSrc: "logo.png",
    description: "Specjalizujemy się w tworzeniu witryn internetowych od strony Frontendu z dużą znajomością HTML, CSS i JS jak i popularnych JavaScriptowych framework'ow takich jak Vue"
  },
  {
    title: "Brand strategy",
    imgSrc: "icon-3.png",
    description: "I help design strong and captivating brand strategies. Through thorough research and market analysis."
  }
];

const works: Work[] = [
  {
    title: "Alana - live data app",
    imgSrc: "alana.png",
    href: "/",
  },
  {
    title: "Wohoo - weather app",
    imgSrc: "wohoo.png",
    href: "/",
  },
  {
    title: "Pagee - real estate UI kit",
    imgSrc: "pagee.png",
    href: "/",
  },
  {
    title: "Keikoko - agency web",
    imgSrc: "keikoko.png",
    href: "/",
  }
];
</script>

<style>

.line {
  background-color: var(--primary);
  width: 50px;
  border: 1.9px;
  height: 2px;
  float: left;
  margin-right: 10px;
  opacity: 1;
}

.services-header-content {
  display: flex;
  align-items: center;
  
}
.services-header-right-block {
  display: flex;
  justify-content: end;
  button {
    font-size: 14px;
    background-color: transparent;
    font-weight: bold;

    padding: 10px 16px;
    border: 1px solid var(--primary);
    color: white;
    cursor: pointer;
    transition: color 0.3s ease-in-out;
    margin-top: 1rem;
  }

  button:hover {
    background-color: var(--primary);
    border-color: var(--lightDark);
    color: var(--lightDark);
  }
}

.services-header-content span {
  color: var(--primary);
  font-weight: bold;
  font-size: 1.25rem;
}

.services-header h2 {
  font-size: 2.5rem;
  font-weight: bold;
  color: var(--white);
}

.services-description {
  font-size: 1.2rem;
  color: var(--gray);
}

@media (max-width: 574px) {
  .services-header h2 {
    font-size: 1.5rem;
  }

  .services-description {
    font-size: 1rem;
  }

  .services-header-content span {
    font-size: 1.1rem;
  }
  .services-header{
    margin-left: 1.2rem;
  }
 
}
@media (max-width: 991px) {
  .services-header-right-block {
    justify-content: start;
  }
  .row{
    display: flex;
    .services-header-content{
      order: 1;
    }
  }
  .container-block{
    display: flex;
    flex-direction: column;
    width: 100%;
    align-items: center;
  }
}
.album{
  background-color: var(--lightDark) !important;

}
.container-block{
  display: flex;
  flex-wrap: wrap;
  width: 100%;
  justify-content: center;
}

/* contact */
.container-contact
.row {
  align-items: center;
  padding: 48px 0;
}

.row
p {
  color: var(--gray);
}



#footer 
.row {
  align-items: center;
}
#footer {
  padding: 48px 0;
  background-color: var(--deepDark);
  margin: 0;
}

#footer a {
  color: var(--primary);
  text-decoration: none;
}

#footer .bi {
  fill: var(--white);
  transition: .3s ease;
}
#footer .bi:hover {
  fill: var(--primary);
}

#footer hr {
  border: none;
  height: 2px;
  background-color: var(--white);
  
}
.footer-header p {
  margin: 0;
}
@media(max-width:995px) {
  .footer-header{
    justify-content: center;
    align-items: center;
    display: flex;
  }
  #footer p {
    margin-bottom: 10px;
  }
}

</style>
