<script setup>

</script>

<template>
  <section class="sobre-nosotros">
    <div class="texto">
      <h2>Sobre nosotros</h2>
      <p>En TrackLab creemos que cada envío importa. Desarrollamos una plataforma que une a empresas proveedoras y clientes en un ecosistema logístico inteligente, donde cada movimiento queda registrado y cada entrega tiene seguimiento.</p>
      <p>Conectamos procesos, personas y paquetes a través de tecnología intuitiva, para que la logística deje de ser una preocupación y se convierta en una ventaja competitiva.</p>
    </div>

    <div class="logo-info">
      <img src="../../assets/tracklab-logo.png" alt="TrackLab Logo">
    </div>
  </section>
</template>

<style scoped>
section.sobre-nosotros {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 60px;
  padding-top: 100px;
  flex-wrap: wrap;
  background: #fff;
}
.texto {
  max-width: 500px;
  text-align: center;
}
.texto h2 {
  color: #333;
  font-size: 32px;
  margin-bottom: 20px;
  font-weight: 700;
}
.texto p {
  font-size: 16px;
  line-height: 1.6;
  color: #333;
  margin-bottom: 10px;
}
.logo-info {
  text-align: center;
}
.logo-info img {
  width: 350px;
  margin-bottom: 10px;
}
.logo-info p {
  font-size: 14px;
  color: #3399FF;
  margin: 0;
}
</style>