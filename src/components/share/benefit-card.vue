<script setup>
defineProps({
  icon: {
    type: String,
    required: true
  },
  title: {
    type: String,
    required: true
  },
  description: {
    type: String,
    required: true
  }
})
</script>

<template>
  <div class="benefit-card">
    <div class="benefit-icon">{{ icon }}</div>
    <div class="benefit-title">{{ title }}</div>
    <div class="benefit-description">{{ description }}</div>
  </div>
</template>

<style scoped>
.benefit-card {
  background: rgba(255, 255, 255, 0.95);
  padding: 2rem;
  border-radius: 20px;
  box-shadow: 0 8px 30px rgba(0, 0, 0, 0.1);
  text-align: center;
  transition: all 0.4s ease;
  backdrop-filter: blur(10px);
  border: 1px solid rgba(255, 255, 255, 0.2);
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 1rem;
}

.benefit-card:hover {
  transform: translateY(-10px);
  box-shadow: 0 15px 35px rgba(0, 0, 0, 0.2);
  background: rgba(255, 255, 255, 0.98);
}

.benefit-icon {
  font-size: 3rem;
  margin-bottom: 1rem;
  transition: transform 0.4s ease;
  display: flex;
  align-items: center;
  justify-content: center;
  width: 80px;
  height: 80px;
  background: rgba(255, 255, 255, 0.9);
  border-radius: 50%;
  box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
}

.benefit-card:hover .benefit-icon {
  transform: scale(1.1) rotate(5deg);
}

.benefit-title {
  color: var(--primary-blue);
  font-size: 1.4rem;
  font-weight: 700;
  margin-bottom: 0.8rem;
  line-height: 1.3;
  letter-spacing: -0.3px;
}

.benefit-description {
  font-size: 1.1rem;
  color: var(--neutral-gray-700);
  line-height: 1.6;
  max-width: 90%;
  margin: 0 auto;
}

@media (max-width: 768px) {
  .benefit-card {
    padding: 1.5rem;
  }

  .benefit-icon {
    font-size: 2.5rem;
    width: 70px;
    height: 70px;
  }

  .benefit-title {
    font-size: 1.2rem;
  }

  .benefit-description {
    font-size: 1rem;
  }
}
</style>
