<script setup>
defineProps({
  title: String,
  text1: String,
  text2: String,
  text3: String,
  text4: String,
  price: Number,
  featured: {
    type: Boolean,
    default: false
  }
})
</script>

<template>
  <div class="card-container" :class="{ 'featured': featured }">
    <div class="featured-badge" v-if="featured">Popular</div>
    <p class="card-title">{{ title }}</p>
    <div class="text-container">
      <p class="card-text">{{ text1 }}</p>
      <p class="card-text">{{ text2 }}</p>
      <p class="card-text">{{ text3 }}</p>
      <p class="card-text">{{ text4 }}</p>
    </div>
    <div class="card-price-container">
      <div class="card-price">{{ 'S/ ' + price }}</div>
      <button class="select-btn">Seleccionar</button>
    </div>
  </div>
</template>

<style scoped>
  .card-container {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    width: 300px;
    min-height: 380px;
    padding: 24px;
    background-color: #fff;
    border-radius: 20px;
    box-shadow: 0 8px 20px rgba(0, 0, 0, 0.05);
    transition: all 0.3s ease;
    position: relative;
    border: 1px solid #f0f0f0;
  }

  .card-container:hover {
    transform: translateY(-5px);
    box-shadow: 0 12px 30px rgba(0, 0, 0, 0.1);
  }

  .featured {
    border: 2px solid #42A5FF;
    transform: scale(1.05);
  }

  .featured:hover {
    transform: translateY(-5px) scale(1.2);
  }

  .featured-badge {
    position: absolute;
    top: -12px;
    right: 20px;
    background-color: #42A5FF;
    color: white;
    font-size: 14px;
    font-weight: bold;
    padding: 4px 12px;
    border-radius: 20px;
    box-shadow: 0 4px 8px rgba(66, 165, 255, 0.3);
  }

  .card-title {
    font-family: Inter, sans-serif;
    font-weight: bold;
    font-size: 24px;
    color: #181818;
    text-align: center;
    margin-bottom: 20px;
  }

  .text-container {
    display: flex;
    flex-direction: column;
    padding: 0px 10px;
    flex-grow: 1;
  }

  .card-text {
    font-family: Inter, sans-serif;
    font-size: 16px;
    color: #181818;
    align-items: center;
    margin: 12px 0px;
    position: relative;
    padding-left: 5px;
  }

  .card-price-container {
    display: flex;
    flex-direction: column;
    align-items: center;
    margin-top: 20px;
  }

  .card-price {
    font-family: Inter, sans-serif;
    font-size: 28px;
    font-weight: bold;
    color: #181818;
    text-align: center;
    background-color: rgba(66, 165, 255, 0.15);
    border-radius: 12px;
    width: 100%;
    padding: 10px 0;
    margin-bottom: 15px;
  }

  .select-btn {
    background-color: #42A5FF;
    color: white;
    border: none;
    border-radius: 30px;
    padding: 12px 24px;
    font-family: Inter, sans-serif;
    font-weight: 600;
    font-size: 16px;
    cursor: pointer;
    transition: all 0.2s ease;
    width: 100%;
  }

  .select-btn:hover {
    background-color: #3089d8;
    transform: scale(1.05);
  }

  @media (max-width: 768px) {
    .card-container {
      width: 90%;
      max-width: 300px;
    }
    
    .featured {
      transform: scale(1);
    }
    
    .featured:hover {
      transform: translateY(-5px) scale(1);
    }
  }
</style>