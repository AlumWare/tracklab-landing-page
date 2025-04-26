<script setup>

</script>

<template>
  <header>
    <div>
      <a href="#" class="logo">
        <img src="../../assets/tracklab-logo.png" alt="TrackLab Logo">
      </a>
    </div>

    <nav>
      <a href="#sobre-nosotros">Sobre nosotros</a>
      <a href="#beneficios">Beneficios</a>
      <a href="#como-funciona">¿Cómo funciona?</a>
    </nav>
  </header>
</template>

<style scoped>
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 10px 30px;
  background-color: #fff;
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
}
.logo {
  display: flex;
  align-items: center;
  text-decoration: none;
}
.logo img {
  width: 250px;
  height: 50px;
  margin-right: 10px;
}
nav {
  display: flex;
  gap: 15px;
}
nav a {
  text-decoration: none;
  background-color: #3399FF;
  color: white;
  padding: 8px 16px;
  border-radius: 8px;
  font-size: 14px;
  font-weight: 500;
  border: 2px solid #2980b9;
  transition: background-color 0.3s, color 0.3s;
}
nav a:hover {
  background-color: #fff;
  color: #3399FF;
}
</style>