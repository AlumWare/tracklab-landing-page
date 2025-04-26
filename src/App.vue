<script setup>
import ChoosePlan from "@/components/sections/choose-plan.vue";
import ProblemSolution from "@/components/sections/problem-solution.vue";
import HeroSection from "@/components/sections/Hero-Section.vue";
import HowItWorks from "@/components/sections/HowItWorks.vue";
</script>

<template>
  <div class="container">
    <problem-solution></problem-solution>
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
