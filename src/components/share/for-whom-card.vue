<script setup>
defineProps({
  name: {
    type: String,
    required: true
  },
  role: {
    type: String,
    required: true
  },
  description: {
    type: String,
    required: true
  },
  imageSrc: {
    type: String,
    required: true
  }
})
</script>

<template>
  <div class="card-container">
    <div class="image-container">
      <img :src="imageSrc" :alt="name" class="profile-image">
    </div>
    <div class="content-container">
      <h3 class="user-name">{{ name }} - <span class="user-role">{{ role }}</span></h3>
      <p class="user-description">{{ description }}</p>
    </div>
  </div>
</template>

<style scoped>
.card-container {
  display: flex;
  flex-direction: column;
  width: 280px;
  border-radius: 12px;
  overflow: hidden;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
  background-color: #ffffff;
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.card-container:hover {
  transform: translateY(-5px);
  box-shadow: 0 8px 16px rgba(0, 0, 0, 0.15);
}

.image-container {
  width: 100%;
  height: 180px;
  overflow: hidden;
}

.profile-image {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.content-container {
  padding: 16px;
}

.user-name {
  font-family: Inter, sans-serif;
  font-size: 16px;
  font-weight: 700;
  color: #181818;
  margin: 0 0 8px 0;
}

.user-role {
  font-weight: 400;
}

.user-description {
  font-family: Inter, sans-serif;
  font-size: 14px;
  line-height: 1.4;
  color: #181818;
  margin: 0;
}
</style>
