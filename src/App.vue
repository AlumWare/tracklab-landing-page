<script setup>
import ChoosePlan from "@/components/sections/choose-plan.vue";
import ProblemSolution from "@/components/sections/problem-solution.vue";
import HeroSection from "@/components/sections/Hero-Section.vue";
import HowItWorks from "@/components/sections/HowItWorks.vue";
import LandingHeader from "@/components/sections/landing-header.vue";
import AboutUs from "@/components/sections/about-us.vue";
import MainBenefits from "@/components/sections/main-benefits.vue";
import Faq from "@/components/sections/faq.vue";
import Footer from "@/components/sections/footer.vue";
import Contact from "@/components/sections/contact.vue";
import ForWhom from "@/components/sections/for-whom.vue";
</script>

<template>
  <div class="container">
    <landing-header></landing-header>
    <hero-section></hero-section>
    <about-us id="sobre-nosotros"></about-us>
    <for-whom id="para-quien"></for-whom>
    <problem-solution id="problema-solucion"></problem-solution>
    <main-benefits id="beneficios"></main-benefits>
    <how-it-works id="como-funciona"></how-it-works>
    <choose-plan id="planes"></choose-plan>
    <Contact id="contacto"></Contact>
    <faq id="preguntas-frecuentes"></faq>
    <Footer />
  </div>
</template>

<style scoped>
  .container {
    display: flex;
    flex-direction: column;
    width: 100%;
    min-height: 100vh;
    margin: 0;
    padding: 0;
    overflow-x: hidden;
  }

  /* Restablecer algunos estilos globales para asegurar que todo funcione correctamente */
  :global(body) {
    margin: 0;
    padding: 0;
    overflow-x: hidden;
  }

  :global(*) {
    box-sizing: border-box;
  }
</style>
