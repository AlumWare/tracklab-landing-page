<script setup>

import PlanCard from "@/components/share/plan-card.vue";
</script>

<template>
<div class="section">
  <div class="title-plan">
    <p class="title">ELEGÍ TU PLAN</p>
    <p class="subtitle">Contamos con múltiples planes acorde a las necesidades de tu empresa</p>
  </div>
  <div class="cards">
    <plan-card
        title="Básico"
        text1="✔ 1 empresa cliente y 1 proveedora"
        text2="✔ Hasta 50 pedidos/mes"
        text3="✔ Soporte dedicado"
        text4="✔ Dashboard básico"
        :price="9990"
    ></plan-card>
    <plan-card
        title="Premium"
        text1="✔ Hasta 5 empresas conectadas"
        text2="✔ 500 pedidos/mes"
        text3="✔ Dashboard avanzado"
        text4="✔ Soporte preferencial"
        :price="24990"
    ></plan-card>
    <plan-card
        title="Enterprise"
        text1="✔ Empresas ilimitadas"
        text2="✔ Envíos ilimitados"
        text3="✔ Soporte dedicado"
        text4="✔ Integraciones personalizadas"
        :price="100"
    ></plan-card>
  </div>
</div>
</template>

<style scoped>
  .section {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    background-color: #42A5FF;
    width: 100%;
    height: 100%;
    padding: 100px;
    gap: 50px;
  }

  .title-plan {
    margin-bottom: 10px;
    text-align: center;
    justify-content: center;
  }

  .title {
    font-family: Inter;
    font-weight: bold;
    font-size: 28px;
    color: #181818;
    text-align: center;
  }

  .subtitle {
    font-family: Inter;
    font-weight: normal;
    font-size: 20px;
    color: #181818;
    text-align: center;
  }

  .cards {
    display: flex;
    flex-direction: row;
    justify-items: space-between;
    gap: 40px;
  }
</style>