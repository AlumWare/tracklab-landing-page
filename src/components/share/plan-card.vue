<script setup>
defineProps({
  title: String,
  text1: String,
  text2: String,
  text3: String,
  text4: String,
  price: Number
})
</script>

<template>
  <div class="card-container">
    <p class="card-title">{{ title }}</p>
    <div class="text-container">
      <p class="card-text">{{ text1 }}</p>
      <p class="card-text">{{ text2 }}</p>
      <p class="card-text">{{ text3 }}</p>
      <p class="card-text">{{ text4 }}</p>
    </div>
    <div class="card-price">{{ 'S/ ' + price }}</div>
  </div>
</template>

<style scoped>
  .card-container {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    width: 268px;
    height: 310px;
    padding: 12px;
    background-color: #fff;
    border-radius: 20px;
  }

  .card-title {
    font-family: Inter;
    font-weight: bold;
    font-size: 20px;
    color: #181818;
    text-align: center;
  }

  .text-container {
    display: flex;
    flex-direction: column;
    padding: 0px 10px;
  }

  .card-text {
    font-family: Inter;
    font-size: 16px;
    justify-content: left;
    color: #181818;
    align-items: center;
    margin: 10px 0px;
  }

  .card-price {
    font-family: Inter;
    font-size: 20px;
    font-weight: bold;
    color: #181818;
    text-align: center;
    justify-content: center;
    align-items: center;
    background-color: #42A5FF;
    border: 2px solid #dcdcdc;
    border-radius: 20px;
    width: 154px;
    height: fit-content;
    margin-top: 5px;
  }
</style>