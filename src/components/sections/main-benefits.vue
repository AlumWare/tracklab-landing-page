<script setup>

</script>

<template>
  <section class="beneficios-principales">
    <h1>Beneficios Principales</h1>

    <div class="benefits-grid">
      <div class="benefit-card">
        <div class="benefit-icon">📍</div>
        <div class="benefit-title">Trazabilidad de extremo a extremo</div>
        <div class="benefit-description">Visualiza en qué estado está cada envío, quién lo gestionó y qué se entregó.</div>
      </div>

      <div class="benefit-card">
        <div class="benefit-icon">📦</div>
        <div class="benefit-title">Confirmación segura de recepción</div>
        <div class="benefit-description">La entrega no termina hasta que el cliente lo confirme. Todo queda asentado.</div>
      </div>

      <div class="benefit-card">
        <div class="benefit-icon">📊</div>
        <div class="benefit-title">Dashboard inteligente</div>
        <div class="benefit-description">Accede a reportes de envíos por estado, por empresa o por fecha en tiempo real.</div>
      </div>

      <div class="benefit-card">
        <div class="benefit-icon">📝</div>
        <div class="benefit-title">Registro de envío digital</div>
        <div class="benefit-description">Crea solicitudes con fotos, detalles y validaciones, desde la aplicación.</div>
      </div>

      <div class="benefit-card">
        <div class="benefit-icon">🤝</div>
        <div class="benefit-title">Colaboración entre empresas</div>
        <div class="benefit-description">Ambas partes pueden interactuar y validar procesos dentro de la misma aplicación.</div>
      </div>

      <div class="benefit-card">
        <div class="benefit-icon">🗂️</div>
        <div class="benefit-title">Historial y documentación automática</div>
        <div class="benefit-description">Olvídate del papeleo. Cada operación queda archivada y disponible cuando lo necesites.</div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.beneficios-principales {
  padding: 10px 0;
  background: #42A5FF;
}
h1 {
  text-align: center;
  font-weight: bold;
  font-size: 2.5rem;
  margin-bottom: 40px;
  color: #000;
}
.benefits-grid {
  padding: 0 20px;
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 30px;
  width: 100%;
  max-width: 1200px;
}
.benefit-card {
  background: white;
  padding: 25px 20px;
  border-radius: 16px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  text-align: center;
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}
.benefit-card:hover {
  transform: translateY(-8px);
  box-shadow: 0 8px 16px rgba(0, 0, 0, 0.15);
}
.benefit-icon {
  font-size: 2rem;
  margin-bottom: 15px;
}
.benefit-title {
  color: #181818;
  font-size: 1.2rem;
  font-weight: bold;
  margin-bottom: 10px;
}
.benefit-description {
  font-size: 0.95rem;
  color: #555;
}
</style>