<script setup>
import PlanCard from "@/components/share/plan-card.vue";
</script>

<template>
<section class="plan-section">
  <div class="plan-container">
    <div class="title-plan">
      <h2 class="title">ELEGÍ TU PLAN</h2>
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
          :featured="true"
      ></plan-card>
      <plan-card
          title="Enterprise"
          text1="✔ Empresas ilimitadas"
          text2="✔ Envíos ilimitados"
          text3="✔ Soporte dedicado"
          text4="✔ Integraciones personalizadas"
          :price="100000"
      ></plan-card>
    </div>
  </div>
</section>
</template>

<style scoped>
  .plan-section {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    background-color: var(--primary-blue);
    background-image: linear-gradient(45deg, var(--primary-blue) 0%, var(--primary-blue-dark) 100%);
    width: 100%;
    min-height: 100vh;
    padding: 100px 20px;
    position: relative;
    overflow: hidden;
  }

  .plan-section::before {
    content: '';
    position: absolute;
    top: -50px;
    left: 0;
    width: 100%;
    height: 100px;
    background-color: #f5f7fa;
    border-radius: 0 0 50% 50%;
  }

  .plan-container {
    max-width: 1200px;
    width: 100%;
    z-index: 1;
  }

  .title-plan {
    margin-bottom: 60px;
    text-align: center;
  }

  .title {
    font-family: Inter, sans-serif;
    font-weight: bold;
    font-size: 42px;
    color: white;
    text-align: center;
    margin-bottom: 15px;
    text-shadow: 0 2px 4px rgba(0,0,0,0.1);
  }

  .subtitle {
    font-family: Inter, sans-serif;
    font-weight: normal;
    font-size: 22px;
    color: white;
    text-align: center;
    max-width: 700px;
    margin: 0 auto;
  }

  .cards {
    display: flex;
    flex-direction: row;
    justify-content: center;
    flex-wrap: wrap;
    gap: 40px;
    padding: 20px 0;
  }

  @media (max-width: 1100px) {
    .cards {
      gap: 30px;
    }
  }

  @media (max-width: 768px) {
    .plan-section {
      padding: 80px 15px;
    }
    
    .title {
      font-size: 32px;
    }
    
    .subtitle {
      font-size: 18px;
    }
    
    .cards {
      flex-direction: column;
      align-items: center;
    }
  }
</style>