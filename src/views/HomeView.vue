<template>
  <SectionHero/>
  <section class="services">
    <div class="services-header">
      <h2>7+ years experience working</h2>
      <div class="services-header-right-block">
        <div class="right-block-wrapper">
          <hr class="line"> 
          Services
        </div>
        <p>Discover the best services I offer, designed to ensure the success of your project.</p>
      </div>
    </div>
    <div class="cardServices">
        <SectionServices v-for="service in services"
        :key="service.title"
        :imgSrc="service.imgSrc" 
        :title="service.title"
        :description="service.description" 
        />
    </div>
  </section>
  <section class="works">
    <div class="top-block">
      <hr class="line"> 
      <span>Recent Work</span>
    </div>
    <div class="works-header">
      <h2>Some of my favorite <br> projects.</h2>
      <div class="services-header-right-block">
        <button>View All Project</button>
      </div>
    </div>
    <!-- wyswieltenie komponentu Section work -->
  </section>
</template>

<script lang="ts" setup>
import SectionHero from "../components/SectionHero.vue";
import SectionServices from "../components/SectionServices.vue";

interface service{
  title:string,
  imgSrc:string,
  description:string,
}

const services: service[] = [
  {
    title: "Product Designer",
    imgSrc: "./assets/icon-1.png",
    description: "I offer innovative and attention-grabbing product design services. From initial ideation to implementation"
  },
  {
    title: "Frontend develop",
    imgSrc: "./assets/icon-2.png",
    description: "Specialize in responsive and interactive front-end development. With a deep understanding of HTML, CSS, and JS."
  },
  {
    title: "Brand strategy",
    imgSrc: "./assets/icon-3.png",
    description: "I help design strong and captivating brand strategies. Through thorough research and market analysis."
  }
];
</script>

<style>
.wrapper{
  width: 100%;
}

.services{
  .cardServices{
    width: 100%;
    justify-content: center;
    display: flex;
  }

  .services-header{
    width: 100%;
    justify-content: space-around;
    display: flex;
    align-items: center;

    .services-header-right-block{
      .right-block-wrapper{
        .line{
          background-color: var(--primary);
          width: 50px;
          border: 1.9px;
          height: 2px;
          float: left;
          margin-right: 10px;
        }
        color: var(--primary);
      }
      p{
        color: var(--gray);
      }
    }
  }
}

h2{
  color: var(--white);
  font-weight: bold;
  font-size: 46px;
  line-height: 56px;
}

.works {
  margin-top: 50px;
  background: var(--lightDark);
  padding: 80px 100px;

  .top-block {
    width: 100%;
    .line {
      background-color: var(--primary);
      width: 50px;
      border: 1.9px;
      height: 2px;
      float: left;
      margin-right: 10px;
    }
    span {
      color: var(--primary);
      font-weight: bold;
    }
  }

  .works-header {
    width: 100%;
    justify-content: space-between;
    display: flex;
    align-items: center;

    h2 {
      margin: 10px 0;
    }

    .services-header-right-block{
      button {
        font-size: 14px;
        background-color: transparent;
        font-weight: bold;
        padding: 10px 16px;
        border: 1px solid var(--primary);
        color: white;
        cursor: pointer;
        transition: color 0.3s ease-in-out;
      }

      button:hover {
        background-color: var(--primary);
        border-color: var(--lightDark);
        color: var(--lightDark);
      }
    }
  }
}
</style>
