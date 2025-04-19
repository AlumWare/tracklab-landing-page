<script setup>
import ChoosePlan from "@/components/sections/choose-plan.vue";
import ProblemSolution from "@/components/sections/problem-solution.vue";
</script>

<template>
  <div class="container">
    <problem-solution></problem-solution>
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
