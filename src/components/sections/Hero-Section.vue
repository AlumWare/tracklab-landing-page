<template>
  <section class="hero">
    <div class="hero-left">
      <h2 class="subtitulo">Trazabilidad logística en tiempo real</h2>
      <h1 class="titulo-tracklab">TrackLab</h1>
      <p class="descripcion">
        Explora nuestro servicio de transporte y tracking en tiempo real.
      </p>
    </div>
    <div class="hero-right">
      <h2 class="titulo-derecha">Enfocado en eficiencia y seguridad</h2>
      <p class="descripcion">Se uno de los primeros en usar este servicio</p>
      <div class="botones">
        <button class="btn">Solicitar Demo</button>
        <button class="btn">Contacto</button>
      </div>
    </div>
  </section>
</template>


<style scoped>
.hero {
  display: flex;
  justify-content: space-between;
  align-items: center;
  background-color: #32aaff;
  padding: 3rem 2rem;
  color: black;
  flex-wrap: wrap;
  min-height: 100vh;
  font-family: sans-serif;
}

.hero-left,
.hero-right {
  flex: 1;
  max-width: 50%;
  padding: 1rem;
}

.titulo-tracklab {
  font-size: 3.5rem;
  font-weight: 900;
  margin: 0.5rem 0;
  position: relative;
  display: inline-block;
}

.titulo-tracklab::after {
  content: '';
  display: block;
  height: 3px;
  width: 100%;
  background-color: black;
  margin-top: 6px;
}


.titulo-derecha {
  font-size: 25px;
  font-weight: 900;
  margin: 0.5rem 0;
}

.subtitulo {
  font-size: 1.4rem;
  font-weight: 700;
  margin-bottom: 0.5rem;
}

.descripcion {
  font-size: 1.1rem;
  margin-top: 0.5rem;
  max-width: 90%;
}

.botones {
  display: flex;
  gap: 1rem;
  margin-top: 1.5rem;
}

.btn {
  background-color: white;
  color: black;
  border: 2px solid black;
  padding: 0.6rem 1.4rem;
  font-size: 1rem;
  font-weight: 600;
  border-radius: 8px;
  cursor: pointer;
  transition: all 0.3s ease;
}

.btn:hover {
  background-color: black;
  color: white;
}

</style>
