<script setup>
import ChoosePlan from "@/components/sections/choose-plan.vue";
import ProblemSolution from "@/components/sections/problem-solution.vue";
import LandingHeader from "@/components/sections/landing-header.vue";
import AboutUs from "@/components/sections/about-us.vue";
import MainBenefits from "@/components/sections/main-benefits.vue";
import Faq from "@/components/sections/faq.vue";
</script>

<template>
  <div class="container">
    <landing-header></landing-header>
    <about-us></about-us>
    <problem-solution></problem-solution>
    <main-benefits></main-benefits>
    <choose-plan></choose-plan>
    <faq></faq>
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
