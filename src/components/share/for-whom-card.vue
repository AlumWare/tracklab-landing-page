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
      <div class="user-info">
        <h3 class="user-name">{{ name }}</h3>
        <span class="user-role">{{ role }}</span>
      </div>
      <p class="user-description">{{ description }}</p>
    </div>
  </div>
</template>

<style scoped>
.card-container {
  display: flex;
  flex-direction: column;
  width: 100%;
  border-radius: 20px;
  overflow: hidden;
  background-color: rgba(255, 255, 255, 0.95);
  box-shadow: 0 8px 30px rgba(0, 0, 0, 0.1);
  backdrop-filter: blur(10px);
  border: 1px solid rgba(255, 255, 255, 0.2);
}

.image-container {
  width: 100%;
  height: 200px;
  overflow: hidden;
  position: relative;
  background: linear-gradient(45deg, var(--primary-blue), var(--primary-blue-dark));
}

.profile-image {
  width: 100%;
  height: 100%;
  object-fit: cover;
  opacity: 0.9;
  transition: transform 0.3s ease, opacity 0.3s ease;
}

.card-container:hover .profile-image {
  transform: scale(1.05);
  opacity: 1;
}

.content-container {
  padding: 1.5rem;
  display: flex;
  flex-direction: column;
  gap: 1rem;
}

.user-info {
  display: flex;
  flex-direction: column;
  gap: 0.5rem;
}

.user-name {
  font-size: 1.4rem;
  font-weight: 700;
  color: var(--primary-blue);
  margin: 0;
  letter-spacing: -0.3px;
  line-height: 1.2;
}

.user-role {
  font-size: 1rem;
  color: var(--neutral-gray-700);
  font-weight: 500;
  line-height: 1.4;
}

.user-description {
  font-size: 1rem;
  line-height: 1.6;
  color: var(--neutral-gray-700);
  margin: 0;
  opacity: 0.9;
}

@media (max-width: 768px) {
  .image-container {
    height: 180px;
  }

  .content-container {
    padding: 1.2rem;
  }

  .user-name {
    font-size: 1.2rem;
  }

  .user-role {
    font-size: 0.95rem;
  }
}

@media (max-width: 480px) {
  .image-container {
    height: 160px;
  }

  .content-container {
    padding: 1rem;
  }
}
</style>
