<template>
<div class="problem-solution-container">
  <div class="content-wrapper">
    <div class="image-container">
      <img src="../../assets/truck.png" alt="Logistics illustration" class="feature-image"/>
    </div>
    <div class="text-container">
      <h2 class="title">{{ $t('p&a.title') }}</h2>
      <div class="problems">
        <h3 class="section-subtitle">{{ $t('p&a.subtitle') }}</h3>
        <ul class="problems-list">
          <li>
            <span class="problem-icon">❌</span>
            <span>{{ $t('p&a.loss') }}</span>
          </li>
          <li>
            <span class="problem-icon">⏱️</span>
            <span>{{ $t('p&a.time') }}</span>
          </li>
          <li>
            <span class="problem-icon">📝</span>
            <span>{{ $t('p&a.mistakes') }}</span>
          </li>
          <li>
            <span class="problem-icon">👥</span>
            <span>{{ $t('p&a.visibility') }}</span>
          </li>
          <li>
            <span class="problem-icon">💰</span>
            <span>{{ $t('p&a.cost') }}</span>
          </li>
        </ul>
      </div>
      <div class="solution">
        <h3 class="section-subtitle">{{ $t('p&a.solution') }}</h3>
        <p class="solution-text">{{ $t('p&a.description') }}</p>
      </div>
    </div>
  </div>
</div>
</template>

<style scoped>
.problem-solution-container {
  min-height: 100vh;
  background: linear-gradient(135deg, var(--neutral-white) 0%, #f5f7fa 100%);
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 6rem 2rem;
}

.content-wrapper {
  display: flex;
  gap: 4rem;
  max-width: 1200px;
  width: 100%;
  align-items: center;
}

.image-container {
  flex: 1;
  display: flex;
  justify-content: center;
  align-items: center;
}

.feature-image {
  max-width: 100%;
  height: auto;
  border-radius: 20px;
  box-shadow: 0 20px 40px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s ease;
}

.feature-image:hover {
  transform: translateY(-10px);
}

.text-container {
  flex: 1;
  max-width: 500px;
  padding: 2rem;
  background: rgba(255, 255, 255, 0.9);
  border-radius: 24px;
  box-shadow: 0 20px 40px rgba(0, 0, 0, 0.05);
  border: 1px solid rgba(0, 0, 0, 0.05);
}

.title {
  font-size: 2.5rem;
  font-weight: 800;
  color: var(--primary-blue);
  margin-bottom: 2rem;
  letter-spacing: -0.5px;
  line-height: 1.2;
}

.section-subtitle {
  font-size: 1.4rem;
  font-weight: 700;
  color: var(--primary-blue-dark);
  margin-bottom: 1rem;
  letter-spacing: -0.3px;
}

.problems {
  margin-bottom: 2rem;
}

.problems-list {
  list-style: none;
  padding: 0;
  display: flex;
  flex-direction: column;
  gap: 1rem;
}

.problems-list li {
  display: flex;
  align-items: center;
  gap: 1rem;
  padding: 0.8rem 1rem;
  color: var(--primary-blue);
  background: rgba(255, 255, 255, 0.8);
  border-radius: 12px;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.03);
  transition: transform 0.2s ease;
}

.problems-list li:hover {
  transform: translateX(10px);
  background: white;
  box-shadow: 0 6px 15px rgba(0, 0, 0, 0.05);
}

.problem-icon {
  font-size: 1.2rem;
  min-width: 24px;
  display: flex;
  align-items: center;
  justify-content: center;
}

.solution {
  padding: 1.5rem;
  background: linear-gradient(135deg, var(--primary-blue) 0%, var(--primary-blue-dark) 100%);
  border-radius: 16px;
  color: white;
}

.solution .section-subtitle {
  color: white;
  margin-bottom: 0.8rem;
}

.solution-text {
  font-size: 1.1rem;
  line-height: 1.6;
  color: rgba(255, 255, 255, 0.95);
}

@media (max-width: 1024px) {
  .content-wrapper {
    flex-direction: column;
    gap: 2rem;
  }

  .text-container {
    max-width: 100%;
  }

  .image-container {
    order: -1;
  }

  .feature-image {
    max-width: 80%;
  }
}

@media (max-width: 768px) {
  .problem-solution-container {
    padding: 4rem 1rem;
  }

  .title {
    font-size: 2rem;
  }

  .section-subtitle {
    font-size: 1.2rem;
  }

  .problems-list li {
    padding: 0.6rem 0.8rem;
  }

  .solution {
    padding: 1.2rem;
  }

  .solution-text {
    font-size: 1rem;
  }
}
</style>