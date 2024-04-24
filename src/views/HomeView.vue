<template>
  <SectionHero />
  <!-- sekcja services -->
  <section class="services ">
    <div class="container">
      <div class="row">
        <div class="col-lg-6">
          <div class="services-header">
            <h2>7+ years experience <br> working</h2>
          </div>
        </div>
        <div class="col-lg-6">
          <div class="services-header">
            <div class="services-header-content">
              <hr class="line"> <span>Services</span> 
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
</template>

<script setup lang="ts">
import SectionHero from "../components/HomeViewComponents/SectionHero.vue";
import sevicesBlock from "@/components/servicesBlock.vue";

import SectionServices from "../components/HomeViewComponents/SectionServices.vue";
import SectionWork from "@/components/HomeViewComponents/SectionWork.vue";
import SectionContact from "@/components/HomeViewComponents/SectionContact.vue";

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
    title: "Frontend develop",
    imgSrc: "icon-2.png",
    description: "Specialize in responsive and interactive front-end development. With a deep understanding of HTML, CSS, and JS."
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
  .row{
    margin-left: 1.2rem;
  }
}
</style>
