<script setup>
import BenefitCard from '../share/benefit-card.vue'
</script>

<template>
  <section class="beneficios-principales">
    <h1>{{ $t('benefits.title') }}</h1>

    <div class="benefits-grid">
      <benefit-card
        icon="📍"
        :title=" $t('benefits.traceability') "
        :description=" $t('benefits.traceability1') "
      />

      <benefit-card
        icon="📦"
        :title=" $t('benefits.confirmation') "
        :description=" $t('benefits.confirmation1') "
      />

      <benefit-card
        icon="📊"
        :title=" $t('benefits.dashboard') "
        :description=" $t('benefits.dashboard1') "
      />

      <benefit-card
        icon="📝"
        :title=" $t('benefits.register') "
        :description=" $t('benefits.register1') "
      />

      <benefit-card
        icon="🤝"
        :title=" $t('benefits.collaboration') "
        :description=" $t('benefits.collaboration1') "
      />

      <benefit-card
        icon="🗂️"
        :title=" $t('benefits.history') "
        :description=" $t('benefits.history1') "
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