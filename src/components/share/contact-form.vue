<template>
  <form class="contact-form" @submit.prevent="submitForm">
    <div class="contact-form__field">
      <input 
        type="text" 
        v-model="name" 
        class="contact-form__input" 
        placeholder="Nombre"
        required
      />
    </div>
    
    <div class="contact-form__field">
      <input 
        type="email" 
        v-model="email" 
        class="contact-form__input" 
        placeholder="Email"
        required
      />
    </div>
    
    <div class="contact-form__field">
      <textarea 
        v-model="message" 
        class="contact-form__textarea" 
        placeholder="Mensaje"
        rows="5"
        required
      ></textarea>
    </div>
    
    <div class="contact-form__submit">
      <button 
        type="submit" 
        class="contact-form__button"
        :disabled="isSubmitting"
      >
        {{ isSubmitting ? 'Enviando...' : 'Enviar' }}
      </button>
    </div>
  </form>
</template>

<script>
export default {
  name: 'ContactForm',
  data() {
    return {
      name: '',
      email: '',
      message: '',
      isSubmitting: false
    }
  },
  methods: {
    submitForm() {
      this.isSubmitting = true;
      
      // Aquí iría la lógica para enviar el formulario a un servidor
      // Por ejemplo, usando fetch o axios para hacer una petición POST
      
      // Simulando el envío del formulario
      setTimeout(() => {
        // Emitir evento para indicar que el formulario se ha enviado
        this.$emit('form-submitted', {
          name: this.name,
          email: this.email,
          message: this.message
        });
        
        // Resetear el formulario
        this.name = '';
        this.email = '';
        this.message = '';
        this.isSubmitting = false;
      }, 1000);
    }
  }
}
</script>

<style scoped>
.contact-form {
  width: 100%;
}

.contact-form__field {
  margin-bottom: 1rem;
}

.contact-form__input,
.contact-form__textarea {
  width: 100%;
  padding: 0.75rem 1rem;
  border: 1px solid #e5e5e5;
  border-radius: 0.25rem;
  background-color: #f5f5f5;
  font-size: 1rem;
  transition: border-color 0.2s, box-shadow 0.2s;
}

.contact-form__input:focus,
.contact-form__textarea:focus {
  outline: none;
  border-color: #4dabf7;
  box-shadow: 0 0 0 3px rgba(77, 171, 247, 0.2);
}

.contact-form__button {
  background-color: #4dabf7;
  color: white;
  border: none;
  border-radius: 1.5rem;
  padding: 0.75rem 2.5rem;
  font-size: 1rem;
  font-weight: 600;
  cursor: pointer;
  transition: background-color 0.2s;
}

.contact-form__button:hover:not(:disabled) {
  background-color: #3a8af7;
}

.contact-form__button:disabled {
  opacity: 0.7;
  cursor: not-allowed;
}
</style> 