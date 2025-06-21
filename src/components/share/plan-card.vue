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
  <div class="plan-card" :class="{ 'featured': featured }">
    <div class="plan-header">
      <h3 class="plan-title">{{ title }}</h3>
      <div class="plan-price">
        <span class="currency">$</span>
        <span class="amount">{{ price }}</span>
        <span class="period">/mes</span>
      </div>
    </div>
    <ul class="plan-features">
      <li>{{ text1 }}</li>
      <li>{{ text2 }}</li>
      <li>{{ text3 }}</li>
      <li>{{ text4 }}</li>
    </ul>
    <a href="https://purple-field-0abcc550f.6.azurestaticapps.net/auth/register" class="plan-button">{{ $t('plan.select') }}</a>
  </div>
</template>

<style scoped>
.plan-card {
  background: white;
  border-radius: 20px;
  padding: 2rem;
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
  transition: all 0.3s ease;
  display: flex;
  flex-direction: column;
  gap: 1.5rem;
  border: 1px solid rgba(0, 0, 0, 0.05);
}

.plan-card.featured {
  transform: scale(1.05);
  border: 2px solid var(--primary-blue);
  box-shadow: 0 15px 40px rgba(0, 0, 0, 0.15);
}

.plan-header {
  text-align: center;
}

.plan-title {
  font-size: 1.5rem;
  font-weight: 700;
  color: var(--primary-blue);
  margin-bottom: 1rem;
}

.plan-price {
  display: flex;
  align-items: baseline;
  justify-content: center;
  gap: 0.2rem;
}

.currency {
  font-size: 1.5rem;
  font-weight: 600;
  color: var(--primary-blue);
}

.amount {
  font-size: 3rem;
  font-weight: 800;
  color: var(--primary-blue);
  line-height: 1;
}

.period {
  font-size: 1rem;
  color: var(--neutral-gray-600);
}

.plan-features {
  list-style: none;
  padding: 0;
  margin: 0;
  display: flex;
  flex-direction: column;
  gap: 1rem;
}

.plan-features li {
  display: flex;
  align-items: center;
  gap: 0.5rem;
  color: var(--neutral-gray-700);
  font-size: 1rem;
}

.plan-features li::before {
  content: '✓';
  color: var(--primary-blue);
  font-weight: bold;
}

.plan-button {
  background: var(--primary-blue);
  color: white;
  text-decoration: none;
  padding: 1rem;
  border-radius: 12px;
  text-align: center;
  font-weight: 600;
  transition: all 0.3s ease;
  margin-top: auto;
}

.plan-button:hover {
  background: var(--primary-blue-dark);
  transform: translateY(-2px);
}

.featured .plan-button {
  background: var(--primary-blue-dark);
}

.featured .plan-button:hover {
  background: var(--primary-blue);
}

@media (max-width: 768px) {
  .plan-card {
    padding: 1.5rem;
  }
  
  .plan-card.featured {
    transform: none;
  }
}
</style>