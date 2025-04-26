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
    <hero-section></hero-section>
    <about-us></about-us>
    <problem-solution></problem-solution>
    <main-benefits></main-benefits>
    <how-it-works></how-it-works>
    <choose-plan></choose-plan>
  </div>
</template>

<style scoped>
  .container {
    display: flex;
    flex-direction: column;
    width: 100%;
  }
</style>
