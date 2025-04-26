<script setup>
import BenefitCard from '../share/benefit-card.vue'
</script>

<template>
  <section class="beneficios-principales">
    <h1>Beneficios Principales</h1>

    <div class="benefits-grid">
      <benefit-card
        icon="📍"
        title="Trazabilidad de extremo a extremo"
        description="Visualiza en qué estado está cada envío, quién lo gestionó y qué se entregó."
      />

      <benefit-card
        icon="📦"
        title="Confirmación segura de recepción"
        description="La entrega no termina hasta que el cliente lo confirme. Todo queda asentado."
      />

      <benefit-card
        icon="📊"
        title="Dashboard inteligente"
        description="Accede a reportes de envíos por estado, por empresa o por fecha en tiempo real."
      />

      <benefit-card
        icon="📝"
        title="Registro de envío digital"
        description="Crea solicitudes con fotos, detalles y validaciones, desde la aplicación."
      />

      <benefit-card
        icon="🤝"
        title="Colaboración entre empresas"
        description="Ambas partes pueden interactuar y validar procesos dentro de la misma aplicación."
      />

      <benefit-card
        icon="🗂️"
        title="Historial y documentación automática"
        description="Olvídate del papeleo. Cada operación queda archivada y disponible cuando lo necesites."
      />
    </div>
  </section>
</template>

<style scoped>
.beneficios-principales {
  min-height: 100vh;
  padding: 100px 2rem;
  background-image: linear-gradient(135deg, var(--primary-blue), var(--primary-blue-dark));
  position: relative;
  overflow: hidden;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.beneficios-principales::before {
  content: '';
  position: absolute;
  top: -50px;
  left: 0;
  width: 100%;
  height: 100px;
  background-color: var(--neutral-white);
  border-radius: 0 0 50% 50%;
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.1);
}

h1 {
  text-align: center;
  font-weight: 800;
  font-size: 3rem;
  margin-bottom: 2rem;
  color: var(--neutral-white);
  position: relative;
  z-index: 1;
  letter-spacing: -0.5px;
}

.benefits-grid {
  padding: 2rem;
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 2rem;
  width: 100%;
  max-width: 1400px;
  margin: 0 auto;
  position: relative;
  z-index: 1;
}

/* Cada benefit-card ocupará un tercio del espacio menos el gap */
:deep(.benefit-card) {
  flex: 0 1 calc(33.333% - 2rem);
  min-width: 300px;
}

@media (max-width: 768px) {
  h1 {
    font-size: 2.5rem;
    margin-bottom: 1.5rem;
  }

  .benefits-grid {
    padding: 1rem;
    gap: 1.5rem;
  }

  :deep(.benefit-card) {
    flex: 0 1 calc(50% - 1.5rem);
    min-width: 280px;
  }
}

@media (max-width: 480px) {
  h1 {
    font-size: 2rem;
  }

  :deep(.benefit-card) {
    flex: 1 1 100%;
  }
}
</style>