<template>
  <section class="how-it-works">
    <h2 class="section-title">¿Cómo funciona TrackLab?</h2>
    <div class="content">
      <div class="video-box">
        <div v-if="!videoVisible" class="video-placeholder" @click="showVideo">
          <img src="../../assets/truck.png" alt="Ver video" />
        </div>
        <div v-else class="video-container">
          <button class="close-btn" @click="hideVideo">✖</button>
          <iframe
              width="100%"
              height="250"
              :src="videoUrl"
              title="Video demostrativo"
              frameborder="0"
              allowfullscreen
          ></iframe>
        </div>
      </div>
      <div class="steps">
        <div class="step">
          <strong>Paso 1: Registrá a tu empresa y tus usuarios</strong>
          <p>Tanto proveedores como clientes se registran desde la app.</p>
        </div>
        <div class="step">
          <strong>Paso 2: Solicitá o recibí un pedido de envío</strong>
          <p>El cliente crea una solicitud y la empresa proveedora la visualiza en su panel.</p>
        </div>
        <div class="step">
          <strong>Paso 3: Gestioná y prepará la carga</strong>
          <p>El proveedor confirma que el pedido está listo y documenta todo digitalmente.</p>
        </div>
        <div class="step">
          <strong>Paso 4: Confirmá la entrega</strong>
          <p>Una vez entregado, el cliente valida la recepción. Todo queda registrado.</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue'

const videoVisible = ref(false)
const videoUrl = ref('')

function showVideo() {
  // Carga la URL con autoplay
  videoUrl.value = 'https://www.youtube.com/embed/dQw4w9WgXcQ?autoplay=1'
  videoVisible.value = true
}

function hideVideo() {
  videoVisible.value = false
  videoUrl.value = '' // Detiene el video limpiando el iframe
}
</script>

<style scoped>
.how-it-works {
  padding: 3rem 2rem;
  background-color: #f9f9f9;
  color: #222;
}

.section-title {
  font-size: 2rem;
  font-weight: bold;
  margin-bottom: 2rem;
  text-align: center;
}

.content {
  display: flex;
  flex-wrap: wrap;
  gap: 2rem;
  align-items: flex-start;
  justify-content: center;
}

.video-box {
  flex: 1;
  min-width: 300px;
  display: flex;
  justify-content: center;
  align-items: center;
  position: relative;
}

.video-placeholder {
  width: 100%;
  max-width: 400px;
  height: 250px;
  background-color: black;
  display: flex;
  justify-content: center;
  align-items: center;
  border-radius: 12px;
  cursor: pointer;
}

.video-placeholder img {
  width: 100px;
}

.video-container {
  position: relative;
  width: 100%;
  max-width: 400px;
}

.close-btn {
  position: absolute;
  top: -10px;
  right: -10px;
  background: white;
  color: red;
  border: none;
  border-radius: 50%;
  width: 28px;
  height: 28px;
  cursor: pointer;
  font-weight: bold;
  z-index: 1;
  box-shadow: 0 0 5px rgba(0,0,0,0.2);
}

.video-container iframe {
  width: 100%;
  height: 250px;
  border-radius: 12px;
}

.steps {
  flex: 1;
  min-width: 300px;
}

.step {
  margin-bottom: 1.5rem;
}

.step strong {
  display: block;
  margin-bottom: 0.25rem;
  font-size: 1.1rem;
}
</style>
