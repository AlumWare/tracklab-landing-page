<script setup>

</script>

<template>
  <section class="sobre-nosotros">
    <div class="content-wrapper">
      <div class="texto">
        <h2>Sobre nosotros</h2>
        <div class="text-content">
          <p>En TrackLab creemos que cada envío importa. Desarrollamos una plataforma que une a empresas proveedoras y clientes en un ecosistema logístico inteligente, donde cada movimiento queda registrado y cada entrega tiene seguimiento.</p>
          <p>Conectamos procesos, personas y paquetes a través de tecnología intuitiva, para que la logística deje de ser una preocupación y se convierta en una ventaja competitiva.</p>
        </div>
      </div>

      <div class="logo-info">
        <div class="logo-container">
          <img src="../../assets/tracklab-logo.png" alt="TrackLab Logo">
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.sobre-nosotros {
  min-height: 100vh;
  background: linear-gradient(135deg, var(--neutral-white) 0%, #f5f7fa 100%);
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 6rem 2rem;
  position: relative;
  overflow: hidden;
}

.content-wrapper {
  max-width: 1200px;
  width: 100%;
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 4rem;
  position: relative;
  z-index: 1;
}

.texto {
  flex: 1;
  max-width: 600px;
  padding: 2rem;
  background: rgba(255, 255, 255, 0.9);
  border-radius: 24px;
  box-shadow: 0 20px 40px rgba(0, 0, 0, 0.05);
  border: 1px solid rgba(0, 0, 0, 0.05);
  transform: translateY(0);
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.texto:hover {
  transform: translateY(-10px);
  box-shadow: 0 30px 60px rgba(0, 0, 0, 0.1);
}

.texto h2 {
  color: var(--primary-blue);
  font-size: 2.5rem;
  margin-bottom: 1.5rem;
  font-weight: 800;
  letter-spacing: -0.5px;
  line-height: 1.2;
}

.text-content {
  display: flex;
  flex-direction: column;
  gap: 1rem;
}

.texto p {
  font-size: 1.1rem;
  line-height: 1.8;
  color: var(--neutral-gray-700);
  margin: 0;
  text-align: left;
}

.logo-info {
  flex: 1;
  max-width: 500px;
  display: flex;
  justify-content: center;
  align-items: center;
}

.logo-container {
  width: 100%;
  padding: 2rem;
  background: white;
  border-radius: 24px;
  box-shadow: 0 20px 40px rgba(0, 0, 0, 0.05);
  transition: transform 0.3s ease;
}

.logo-container:hover {
  transform: scale(1.05);
}

.logo-info img {
  width: 100%;
  max-width: 400px;
  height: auto;
  display: block;
  margin: 0 auto;
}

@media (max-width: 1024px) {
  .content-wrapper {
    flex-direction: column;
    gap: 3rem;
  }

  .texto, .logo-info {
    max-width: 100%;
  }

  .logo-container {
    max-width: 400px;
    margin: 0 auto;
  }
}

@media (max-width: 768px) {
  .sobre-nosotros {
    padding: 4rem 1rem;
  }

  .texto {
    padding: 1.5rem;
  }

  .texto h2 {
    font-size: 2rem;
    margin-bottom: 1rem;
  }

  .texto p {
    font-size: 1rem;
    line-height: 1.6;
  }

  .logo-container {
    padding: 1.5rem;
  }
}

@media (max-width: 480px) {
  .texto h2 {
    font-size: 1.8rem;
  }

  .logo-info img {
    max-width: 300px;
  }
}
</style>