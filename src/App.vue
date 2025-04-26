<script setup>
import ChoosePlan from "@/components/sections/choose-plan.vue";
import ProblemSolution from "@/components/sections/problem-solution.vue";
import HeroSection from "@/components/sections/Hero-Section.vue";
import HowItWorks from "@/components/sections/HowItWorks.vue";
import LandingHeader from "@/components/sections/landing-header.vue";
import AboutUs from "@/components/sections/about-us.vue";
import MainBenefits from "@/components/sections/main-benefits.vue";
</script>

<template>
  <div class="container">
    <landing-header></landing-header>
    <about-us></about-us>
    <problem-solution></problem-solution>
    <main-benefits></main-benefits>
    <choose-plan></choose-plan>
    <hero-section></hero-section>
    <how-it-works></how-it-works>
  </div>
</template>

<style scoped>
  .container {
    display: flex;
    flex-direction: column;
    width: 100%;
  }
</style>
