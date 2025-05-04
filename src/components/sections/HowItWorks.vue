<template>
  <section class="how-it-works">
    <h2 class="section-title">{{ $t('how.title') }}</h2>
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
          <strong>{{ $t('how.step1') }}</strong>
          <p>{{ $t('how.desc1') }}</p>
        </div>
        <div class="step">
          <strong>{{ $t('how.step2') }}</strong>
          <p>{{ $t('how.desc2') }}</p>
        </div>
        <div class="step">
          <strong>{{ $t('how.step3') }}</strong>
          <p>{{ $t('how.desc3') }}.</p>
        </div>
        <div class="step">
          <strong>{{ $t('how.step4') }}</strong>
          <p>{{ $t('how.desc4') }}</p>
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
  min-height: 100vh;
  padding: 100px 2rem 4rem;
  background-color: var(--neutral-white);
  color: var(--neutral-black);
  position: relative;
  overflow: hidden;
}

.section-title {
  font-size: 3rem;
  font-weight: 800;
  margin-bottom: 4rem;
  text-align: center;
  letter-spacing: -0.5px;
  line-height: 1.2;
}

.content {
  display: flex;
  flex-wrap: wrap;
  gap: 4rem;
  align-items: center;
  justify-content: center;
  max-width: 1400px;
  margin: 0 auto;
  padding: 0 2rem;
}

.video-box {
  flex: 1;
  min-width: 350px;
  max-width: 600px;
}

.video-placeholder {
  width: 100%;
  aspect-ratio: 16/9;
  background: linear-gradient(45deg, var(--primary-blue), var(--primary-blue-dark));
  display: flex;
  justify-content: center;
  align-items: center;
  border-radius: 20px;
  cursor: pointer;
  transition: all 0.4s ease;
  box-shadow: 0 8px 30px rgba(0, 0, 0, 0.1);
  position: relative;
  overflow: hidden;
}

.video-placeholder::before {
  content: '';
  position: absolute;
  width: 100%;
  height: 100%;
  background: rgba(255, 255, 255, 0.1);
  transform: translateX(-100%);
  transition: transform 0.6s ease;
}

.video-placeholder:hover::before {
  transform: translateX(100%);
}

.video-placeholder img {
  width: 140px;
  filter: drop-shadow(0 4px 6px rgba(0, 0, 0, 0.2));
  transition: transform 0.4s ease;
}

.video-placeholder:hover img {
  transform: scale(1.15);
}

.steps {
  flex: 1;
  min-width: 350px;
  max-width: 600px;
}

.step {
  margin-bottom: 2.5rem;
  padding: 2rem;
  background: white;
  border-radius: 16px;
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.06);
  transition: all 0.3s ease;
  border: 1px solid rgba(0, 0, 0, 0.05);
}

.step:hover {
  transform: translateX(8px);
  box-shadow: 0 6px 25px rgba(0, 0, 0, 0.08);
}

.step strong {
  display: block;
  margin-bottom: 0.8rem;
  font-size: 1.4rem;
  color: var(--primary-blue);
  font-weight: 700;
  letter-spacing: -0.3px;
}

.step p {
  color: var(--neutral-gray-700);
  line-height: 1.6;
  font-size: 1.1rem;
  opacity: 0.9;
}

.video-container {
  width: 100%;
  aspect-ratio: 16/9;
  position: relative;
}

.close-btn {
  position: absolute;
  top: -18px;
  right: -18px;
  background: white;
  color: var(--primary-blue);
  border: none;
  border-radius: 50%;
  width: 36px;
  height: 36px;
  cursor: pointer;
  font-weight: bold;
  z-index: 1;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.15);
  transition: all 0.3s ease;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 1.2rem;
}

.close-btn:hover {
  transform: scale(1.1) rotate(90deg);
  background: var(--primary-blue);
  color: white;
}

.video-container iframe {
  width: 100%;
  height: 100%;
  border-radius: 20px;
  box-shadow: 0 8px 30px rgba(0, 0, 0, 0.1);
}

@media (max-width: 768px) {
  .section-title {
    font-size: 2.2rem;
    margin-bottom: 3rem;
  }
  
  .content {
    gap: 3rem;
    padding: 0 1rem;
  }
  
  .step {
    padding: 1.5rem;
  }
  
  .step strong {
    font-size: 1.2rem;
  }
  
  .step p {
    font-size: 1rem;
  }
}

@media (max-width: 480px) {
  .section-title {
    font-size: 2rem;
  }
  
  .video-box, .steps {
    min-width: 300px;
  }
}
</style>
