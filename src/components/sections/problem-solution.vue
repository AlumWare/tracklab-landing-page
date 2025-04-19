<template>
<div class="problem-solution-container">
  <img src="../../assets/truck.png" height="250" width="500"/>
  <div class="text-container">
    <p class="title">Problemática y Solución</p>
    <div class="problems">
      <p class="problems-title">Problemas comunes:</p>
      <ul class="problems-content">
        <li>Pérdida de productos o paquetes sin rastreo</li>
        <li>Tiempos muertos por falta de trazabilidad</li>
        <li>Errores en entregas o documentación manual</li>
        <li>Falta de visibilidad entre áreas internas</li>
        <li>Costo operativo innecesario</li>
      </ul>
    </div>
    <div class="solution">
      <p class="solution-title">Nuestra solución:</p>
      <p class="solution-text">Con TrackLab centralizás toda tu operación logística en una plataforma ágil, intuitiva y en tiempo real. Desde el escaneo de códigos hasta reportes automáticos, AlumWare te muestra todo lo que ocurre.</p>
    </div>
  </div>
</div>
</template>

<style scoped>
  .problem-solution-container {
    background-color: white;
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
    width: 100%;
    height: fit-content;
    padding: 50px 100px;
    gap: 50px;
  }

  .text-container {
    display: flex;
    flex-direction: column;
    color: #181818;
    font-family: Inter;
    width: 400px;
  }

  .title {
    font-weight: bold;
    font-size: 28px;
    color: #181818;
    text-align: center;
    margin-bottom: 25px;
  }

  .problems, .solution {
    font-weight: normal;
    font-size: 16px;
    color: #181818;
    text-align: left;
    margin-bottom: 10px;
  }

  .solution-title, .problems-title {
    margin-bottom: 4px;
    font-size: 18px;
  }
</style>