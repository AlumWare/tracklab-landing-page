<script setup>
import ForWhomCard from "@/components/share/for-whom-card.vue";
</script>

<template>
  <section class="for-whom-section">
    <div class="section-container">
      <h2 class="section-title">¿Para quién es TrackLab?</h2>
      <p class="section-description">Nuestra plataforma está diseñada para diversos roles en empresas de logística y transporte.</p>
      
      <div class="cards-container">
        <for-whom-card
          name="Carlos"
          role="Responsable de distribución en empresa de transporte"
          description="Carlos coordina envíos y retiros en múltiples rutas. Tiene problemas cuando los choferes olvidan reportar entregas, y cuando los productos están en tránsito o entregados."
          imageSrc="/src/assets/truck.png"
        />
        
        <for-whom-card
          name="Marcela"
          role="Gerente de operaciones logísticas"
          description="Marcela supervisa la cadena de suministro de toda la empresa. Necesita reportes claros y en tiempo real para optimizar rutas y reducir costos operativos."
          imageSrc="/src/assets/truck.png"
        />
        
        <for-whom-card
          name="Pedro"
          role="Encargado de recepción de mercadería"
          description="Pedro debe validar y documentar cada recepción de productos. Necesita una forma rápida de confirmar entregas y reportar inconsistencias."
          imageSrc="/src/assets/truck.png"
        />
      </div>
    </div>
  </section>
</template>

<style scoped>
.for-whom-section {
  padding: 4rem 2rem;
  background-color: #f5f7fa;
}

.section-container {
  max-width: 1200px;
  margin: 0 auto;
}

.section-title {
  font-size: 2.5rem;
  font-weight: 700;
  color: #181818;
  text-align: center;
  margin-bottom: 1rem;
}

.section-description {
  font-size: 1.1rem;
  color: #555;
  text-align: center;
  max-width: 700px;
  margin: 0 auto 3rem auto;
}

.cards-container {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 2rem;
}

@media (max-width: 768px) {
  .section-title {
    font-size: 2rem;
  }
  
  .cards-container {
    flex-direction: column;
    align-items: center;
  }
}
</style> 