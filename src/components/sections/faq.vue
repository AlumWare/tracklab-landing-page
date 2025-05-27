<template>
  <section class="faq-section">
    <div class="container">
      <h2 class="section-title">{{ $t('q&a.title') }}</h2>
      <div class="faq-container">
        <extension-panel 
          :title="$t('questions.q1')"
          :initially-open="false"
        >
          <p>{{ $t('questions.a1') }}</p>
        </extension-panel>

        <extension-panel
          :title="$t('questions.q2')"
          :initially-open="false"
        >
          <p>{{ $t('questions.a2') }}</p>
        </extension-panel>

        <extension-panel
            :title="$t('questions.q3')"
            :initially-open="false"
        >
          <p>{{ $t('questions.a3') }}</p>
        </extension-panel>

        <extension-panel
            :title="$t('questions.q4')"
            :initially-open="false"
        >
          <p>{{ $t('questions.a4') }}</p>
        </extension-panel>
      </div>
    </div>
  </section>
</template>

<script>
import ExtensionPanel from '../share/extension-panel.vue';

export default {
  name: 'FaqSection',
  components: {
    ExtensionPanel
  }
}
</script>

<style scoped>
.faq-section {
  min-height: 100vh;
  padding: 4rem 1rem;
  background-color: var(--primary-blue);
  background-image: linear-gradient(45deg, var(--primary-blue) 0%, var(--primary-blue-dark) 100%);
  position: relative;
  padding-top: 100px;
}

.faq-section::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100px;
  background-color: var(--neutral-white);
  border-radius: 0 0 50% 50%;
  z-index: 1;
}

.container {
  max-width: 960px;
  margin: 0 auto;
  position: relative;
  z-index: 1;
}

.section-title {
  color: #fff;
  text-align: center;
  font-size: 2.5rem;
  margin-bottom: 2.5rem;
  font-weight: 700;
}

.faq-container {
  background: rgba(255, 255, 255, 0.9);
  border-radius: 12px;
  padding: 1.5rem;
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
  overflow: visible;
}

@media (max-width: 768px) {
  .section-title {
    font-size: 2rem;
    margin-bottom: 2rem;
  }
  
  .faq-container {
    padding: 1rem;
  }
}
</style>
