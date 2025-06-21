<template>
  <section class="hero">
    <div class="hero-content">
      <div class="hero-left">
        <div class="language-container">
          <language-switcher></language-switcher>
        </div>
        <span class="badge">{{ $t('header.innovation') }}</span>
        <h2 class="subtitulo">{{ $t('header.traceability') }}</h2>
        <h1 class="titulo-tracklab">TrackLab</h1>
        <p class="descripcion">
          {{ $t('header.revolutionize') }}
        </p>
        <div class="stats">
          <div class="stat-item">
            <span class="stat-number">99%</span>
            <span class="stat-label">{{ $t('header.precision') }}</span>
          </div>
          <div class="stat-item">
            <span class="stat-number">24/7</span>
            <span class="stat-label">{{ $t('header.monitoring') }}</span>
          </div>
          <div class="stat-item">
            <span class="stat-number">+500</span>
            <span class="stat-label">{{ $t('header.companies') }}</span>
          </div>
        </div>
      </div>
      <div class="hero-right">
        <div class="content-box">
          <h2 class="titulo-derecha">{{ $t('header.focused') }}</h2>
          <p class="descripcion">{{ $t('header.join') }}</p>
          <div class="botones">
            <a href="https://purple-field-0abcc550f.6.azurestaticapps.net/auth/register" class="btn btn-primary">{{ $t('header.request') }}</a>
            <a href="https://purple-field-0abcc550f.6.azurestaticapps.net/auth/login" class="btn btn-secondary">{{ $t('header.contact') }}</a>
          </div>
          <div class="trust-indicators">
            <span>{{ '🔒' + $t('header.security') }}</span>
            <span>{{ '🚀' + $t('header.implementation') }}</span>
            <span>{{ '💡' + $t('header.support') }}</span>
          </div>
        </div>
      </div>
    </div>
    <div class="hero-shapes">
      <div class="shape shape-1"></div>
      <div class="shape shape-2"></div>
      <div class="shape shape-3"></div>
    </div>
  </section>
</template>

<style scoped>
.hero {
  min-height: 100vh;
  background: linear-gradient(135deg, var(--primary-blue) 0%, var(--primary-blue-dark) 100%);
  position: relative;
  overflow: hidden;
  padding: calc(80px + 4rem) 2rem 4rem;
  display: flex;
  align-items: center;
  justify-content: center;
}

.hero-content {
  max-width: 1400px;
  width: 100%;
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 4rem;
  position: relative;
  z-index: 2;
}

.hero-left, .hero-right {
  flex: 1;
  position: relative;
}

.badge {
  background: rgba(255, 255, 255, 0.1);
  padding: 0.5rem 1rem;
  border-radius: 50px;
  font-size: 0.9rem;
  color: white;
  display: inline-block;
  margin-bottom: 1.5rem;
  backdrop-filter: blur(10px);
  border: 1px solid rgba(255, 255, 255, 0.2);
  margin-top: 20px;
}

.subtitulo {
  font-size: 1.6rem;
  font-weight: 600;
  color: rgba(255, 255, 255, 0.9);
  margin-bottom: 1rem;
  letter-spacing: -0.5px;
}

.titulo-tracklab {
  font-size: 5rem;
  font-weight: 900;
  background: linear-gradient(135deg, #ffffff 0%, rgba(255,255,255,0.85) 100%);
  -webkit-background-clip: text;
  background-clip: text;
  -webkit-text-fill-color: transparent;
  margin: 0.5rem 0 1.5rem;
  line-height: 1.1;
  letter-spacing: -2px;
  position: relative;
  display: inline-block;
}

.titulo-tracklab::after {
  content: '';
  position: absolute;
  bottom: -10px;
  left: 0;
  width: 100%;
  height: 4px;
  background: linear-gradient(90deg, rgba(255,255,255,0.3) 0%, rgba(255,255,255,0.7) 50%, rgba(255,255,255,0.3) 100%);
  border-radius: 2px;
}

.descripcion {
  font-size: 1.2rem;
  color: rgba(255, 255, 255, 0.8);
  line-height: 1.6;
  margin-bottom: 2rem;
  max-width: 90%;
}

.stats {
  display: flex;
  gap: 2rem;
  margin-top: 3rem;
}

.stat-item {
  display: flex;
  flex-direction: column;
  gap: 0.5rem;
}

.stat-number {
  font-size: 2.5rem;
  font-weight: 800;
  color: white;
  line-height: 1;
}

.stat-label {
  font-size: 0.9rem;
  color: rgba(255, 255, 255, 0.7);
  text-transform: uppercase;
  letter-spacing: 1px;
}

.content-box {
  background: rgba(255, 255, 255, 0.1);
  backdrop-filter: blur(10px);
  border: 1px solid rgba(255, 255, 255, 0.2);
  padding: 2.5rem;
  border-radius: 24px;
  box-shadow: 0 20px 40px rgba(0, 0, 0, 0.1);
}

.titulo-derecha {
  font-size: 2rem;
  font-weight: 700;
  color: white;
  margin-bottom: 1rem;
  line-height: 1.3;
}

.botones {
  display: flex;
  gap: 1rem;
  margin: 2rem 0;
}

.btn {
  padding: 0.8rem 1.8rem;
  font-size: 1rem;
  font-weight: 600;
  border-radius: 12px;
  cursor: pointer;
  transition: all 0.3s ease;
  border: none;
}

.btn-primary {
  background: white;
  color: var(--primary-blue);
}

.btn-primary:hover {
  transform: translateY(-3px);
  box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
}

.btn-secondary {
  background: rgba(255, 255, 255, 0.1);
  color: white;
  backdrop-filter: blur(10px);
  border: 1px solid rgba(255, 255, 255, 0.2);
}

.btn-secondary:hover {
  background: rgba(255, 255, 255, 0.2);
  transform: translateY(-3px);
}

.trust-indicators {
  display: flex;
  flex-direction: column;
  gap: 0.8rem;
  margin-top: 2rem;
  color: rgba(255, 255, 255, 0.8);
  font-size: 0.9rem;
}

.trust-indicators span {
  display: flex;
  align-items: center;
  gap: 0.5rem;
}

.hero-shapes {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  z-index: 1;
  overflow: hidden;
  pointer-events: none;
}

.shape {
  position: absolute;
  background: linear-gradient(135deg, rgba(255,255,255,0.1) 0%, rgba(255,255,255,0.05) 100%);
  border-radius: 50%;
  backdrop-filter: blur(10px);
}

.shape-1 {
  width: 500px;
  height: 500px;
  top: -150px;
  right: -100px;
  animation: float1 20s ease-in-out infinite;
}

.shape-2 {
  width: 300px;
  height: 300px;
  bottom: 50px;
  left: -50px;
  animation: float2 15s ease-in-out infinite;
}

.shape-3 {
  width: 250px;
  height: 250px;
  top: 40%;
  right: 25%;
  animation: float3 18s ease-in-out infinite;
}

@keyframes float1 {
  0% {
    transform: translate(0, 0) rotate(0deg);
  }
  33% {
    transform: translate(-40px, 40px) rotate(5deg);
  }
  66% {
    transform: translate(40px, -40px) rotate(-5deg);
  }
  100% {
    transform: translate(0, 0) rotate(0deg);
  }
}

@keyframes float2 {
  0% {
    transform: translate(0, 0) rotate(0deg);
  }
  33% {
    transform: translate(40px, -30px) rotate(-3deg);
  }
  66% {
    transform: translate(-30px, 40px) rotate(3deg);
  }
  100% {
    transform: translate(0, 0) rotate(0deg);
  }
}

@keyframes float3 {
  0% {
    transform: translate(0, 0) rotate(0deg);
  }
  33% {
    transform: translate(-30px, -30px) rotate(3deg);
  }
  66% {
    transform: translate(30px, 30px) rotate(-3deg);
  }
  100% {
    transform: translate(0, 0) rotate(0deg);
  }
}

@media (max-width: 1200px) {
  .hero-content {
    gap: 3rem;
  }
  
  .titulo-tracklab {
    font-size: 4rem;
  }
}

@media (max-width: 968px) {
  .hero-content {
    flex-direction: column;
    text-align: center;
    gap: 3rem;
  }

  .hero-left, .hero-right {
    flex: none;
    width: 100%;
  }

  .descripcion {
    margin: 1rem auto;
  }

  .stats {
    justify-content: center;
  }

  .content-box {
    max-width: 600px;
    margin: 0 auto;
  }

  .botones {
    justify-content: center;
  }
}

@media (max-width: 768px) {
  .hero {
    padding: calc(70px + 2rem) 1rem 2rem;
  }

  .titulo-tracklab {
    font-size: 4rem;
  }

  .stats {
    flex-direction: column;
    gap: 1.5rem;
    align-items: center;
  }

  .botones {
    flex-direction: column;
  }

  .btn {
    width: 100%;
  }
}

@media (max-width: 480px) {
  .hero {
    padding: 2rem 1rem;
  }

  .titulo-tracklab {
    font-size: 3rem;
  }

  .stats {
    flex-direction: column;
    gap: 1.5rem;
    align-items: center;
  }

  .botones {
    flex-direction: column;
  }

  .btn {
    width: 100%;
  }

  .language-container {
    height: 100%;
    display: flex;
    align-items: flex-start;
    justify-content: left;
  }
}
</style>

<script setup lang="ts">
import LanguageSwitcher from "@/components/share/language-switcher.vue";
</script>