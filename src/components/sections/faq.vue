<template>
  <section class="faq-section">
    <div class="container">
      <h2 class="section-title">Preguntas Frecuentes</h2>
      <div class="faq-container">
        <extension-panel 
          title="1. ¿Qué necesito para usar la app?"
          :initially-open="false"
        >
          <p>Para usar nuestra aplicación solo necesitas un dispositivo con conexión a internet 
          (smartphone, tablet o computadora) y crear una cuenta gratuita. No se requiere ninguna 
          instalación adicional ya que funciona directamente desde el navegador web.</p>
        </extension-panel>

        <extension-panel 
          title="2. ¿Puedo conectar mi empresa con varios clientes o proveedores?"
          :initially-open="false"
        >
          <p>Sí, nuestra plataforma está diseñada para permitir que tu empresa se conecte con múltiples 
          clientes y proveedores simultáneamente. Puedes gestionar todas estas relaciones desde un 
          único panel de control, lo que facilita la comunicación y la colaboración.</p>
        </extension-panel>

        <extension-panel 
          title="3. ¿Tiene integración con otras plataformas?"
          :initially-open="false"
        >
          <p>Nuestra aplicación se integra con una amplia variedad de plataformas y servicios populares,
          incluyendo sistemas CRM, herramientas de contabilidad, plataformas de e-commerce y más.
          Si necesitas una integración específica, contacta con nuestro equipo de soporte para verificar
          la disponibilidad o solicitar su desarrollo.</p>
        </extension-panel>

        <extension-panel 
          title="4. ¿Ofrecen soporte o capacitación?"
          :initially-open="false"
        >
          <p>Ofrecemos soporte técnico completo a través de múltiples canales (chat, email y teléfono)
          durante horas laborables. Además, proporcionamos recursos de capacitación gratuitos como 
          tutoriales en video, guías detalladas y webinars regulares para que puedas aprovechar al
          máximo todas las funcionalidades de nuestra plataforma.</p>
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
  background-color: var(--primary-blue);
  border-radius: 0 0 50% 50%;
  z-index: 1;
}

.faq-section::after {
  bottom: -60px;
  transform: translateY(50%);
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
