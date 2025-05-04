<template>
  <section class="contact-section">
    <div class="contact-section__container">
      <div class="contact-section__form-column">
        <h2 class="contact-section__title">Contacto</h2>
        <contact-form @form-submitted="handleFormSubmit" />
      </div>
      
      <div class="contact-section__info-column">
        <div class="contact-section__info-card">
          <h3 class="contact-section__info-title">{{ $t('contact2.title') }}</h3>
          <p class="contact-section__info-text">
            {{ $t('contact2.subtitle') }}
          </p>
          
          <div class="contact-section__contact-item">
            <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" viewBox="0 0 16 16" class="contact-section__icon">
              <path d="M.05 3.555A2 2 0 0 1 2 2h12a2 2 0 0 1 1.95 1.555L8 8.414.05 3.555ZM0 4.697v7.104l5.803-3.558L0 4.697ZM6.761 8.83l-6.57 4.027A2 2 0 0 0 2 14h12a2 2 0 0 0 1.808-1.144l-6.57-4.027L8 9.586l-1.239-.757Zm3.436-.586L16 11.801V4.697l-5.803 3.546Z"/>
            </svg>
            <span>TrackLab@gmail.com</span>
          </div>
          
          <div class="contact-section__contact-item">
            <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" viewBox="0 0 16 16" class="contact-section__icon">
              <path d="M1.885.511a1.745 1.745 0 0 1 2.61.163L6.29 2.98c.329.423.445.974.315 1.494l-.547 2.19a.678.678 0 0 0 .178.643l2.457 2.457a.678.678 0 0 0 .644.178l2.189-.547a1.745 1.745 0 0 1 1.494.315l2.306 1.794c.829.645.905 1.87.163 2.611l-1.034 1.034c-.74.74-1.846 1.065-2.877.702a18.634 18.634 0 0 1-7.01-4.42 18.634 18.634 0 0 1-4.42-7.009c-.362-1.03-.037-2.137.703-2.877L1.885.511z"/>
            </svg>
            <span>+51 956 518 291</span>
          </div>
          
          <div class="contact-section__social-container">
            <social-icons :icon-color="'#4dabf7'" :background-color="'white'" />
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import ContactForm from '../share/contact-form.vue';
import SocialIcons from '../share/social-icons.vue';

export default {
  name: 'ContactSection',
  components: {
    ContactForm,
    SocialIcons
  },
  methods: {
    handleFormSubmit(formData) {
      // Aquí puedes manejar el envío del formulario
      console.log('Formulario enviado:', formData);
      // Mostrar mensaje de éxito o error
      alert('Mensaje enviado correctamente');
    }
  }
}
</script>

<style scoped>
.contact-section {
  min-height: 100vh;
  padding-top: 100px;
  background-color: var(--neutral-white);
  position: relative;
}


.contact-section__container {
  display: flex;
  flex-wrap: wrap;
  max-width: 1200px;
  margin: 0 auto;
  gap: 2rem;
}

.contact-section__form-column {
  flex: 1 1 500px;
}

.contact-section__info-column {
  flex: 1 1 400px;
  display: flex;
  align-items: stretch;
}

.contact-section__title {
  font-size: 2.5rem;
  font-weight: 700;
  margin-bottom: 2rem;
  color: #333;
}

.contact-section__info-card {
  background-color: #4dabf7;
  border-radius: 1rem;
  padding: 2rem;
  color: white;
  width: 100%;
  display: flex;
  flex-direction: column;
}

.contact-section__info-title {
  font-size: 1.5rem;
  font-weight: 600;
  margin-bottom: 1rem;
}

.contact-section__info-text {
  margin-bottom: 1.5rem;
  line-height: 1.5;
}

.contact-section__contact-item {
  display: flex;
  align-items: center;
  margin-bottom: 1rem;
  font-size: 1rem;
}

.contact-section__icon {
  margin-right: 0.75rem;
}

.contact-section__social-container {
  margin-top: auto;
  padding-top: 1.5rem;
}

@media (max-width: 768px) {
  .contact-section__container {
    flex-direction: column;
  }
  
  .contact-section__info-column {
    order: -1;
  }
}
</style>
