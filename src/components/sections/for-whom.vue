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
  min-height: 100vh;
  padding: 100px 2rem;
  background-image: linear-gradient(135deg, var(--primary-blue), var(--primary-blue-dark));
  position: relative;
  overflow: hidden;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.for-whom-section::before {
  content: '';
  position: absolute;
  top: -50px;
  left: 0;
  width: 100%;
  height: 100px;
  background-color: var(--neutral-white);
  border-radius: 0 0 50% 50%;
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.1);
  z-index: 1;
}

.section-container {
  max-width: 1400px;
  margin: 0 auto;
  width: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  position: relative;
  z-index: 2;
}

.section-title {
  text-align: center;
  font-weight: 800;
  font-size: 3rem;
  margin-bottom: 1.5rem;
  color: var(--neutral-white);
  letter-spacing: -0.5px;
}

.section-description {
  font-size: 1.2rem;
  color: rgba(255, 255, 255, 0.9);
  text-align: center;
  max-width: 700px;
  margin: 0 auto 3rem auto;
  line-height: 1.6;
}

.cards-container {
  padding: 2rem;
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 2rem;
  width: 100%;
}

/* Control del tamaño de las cards */
:deep(.card-container) {
  flex: 0 1 calc(33.333% - 2rem);
  min-width: 300px;
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

:deep(.card-container:hover) {
  transform: translateY(-10px);
  box-shadow: 0 8px 30px rgba(0, 0, 0, 0.15);
}

@media (max-width: 768px) {
  .for-whom-section {
    padding: 80px 1rem;
  }

  .section-title {
    font-size: 2.5rem;
    margin-bottom: 1rem;
  }

  .section-description {
    font-size: 1.1rem;
    margin-bottom: 2rem;
  }

  .cards-container {
    padding: 1rem;
    gap: 1.5rem;
  }

  :deep(.card-container) {
    flex: 0 1 calc(50% - 1.5rem);
    min-width: 280px;
  }
}

@media (max-width: 480px) {
  .section-title {
    font-size: 2rem;
  }

  .section-description {
    font-size: 1rem;
  }

  :deep(.card-container) {
    flex: 1 1 100%;
  }
}
</style> 