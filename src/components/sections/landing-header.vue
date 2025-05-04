<script setup>
import { ref, onMounted, onUnmounted } from 'vue'

const isScrolled = ref(false)
const lastScroll = ref(0)
const isVisible = ref(true)
const isMenuOpen = ref(false)

const handleScroll = () => {
  const currentScroll = window.pageYOffset
  isScrolled.value = currentScroll > 20
  isVisible.value = lastScroll.value > currentScroll || currentScroll < 50
  lastScroll.value = currentScroll
}

const toggleMenu = () => {
  isMenuOpen.value = !isMenuOpen.value
  if (isMenuOpen.value) {
    document.body.style.overflow = 'hidden'
  } else {
    document.body.style.overflow = ''
  }
}

const closeMenu = () => {
  isMenuOpen.value = false
  document.body.style.overflow = ''
}

onMounted(() => {
  window.addEventListener('scroll', handleScroll)
})

onUnmounted(() => {
  window.removeEventListener('scroll', handleScroll)
  document.body.style.overflow = ''
})
</script>

<template>
  <header :class="{ 'scrolled': isScrolled, 'hidden': !isVisible }">
    <nav class="nav-container">
      <a href="#" class="logo" @click="closeMenu">
        <img src="../../assets/tracklab-logo.png" alt="TrackLab Logo">
      </a>

      <!-- Desktop Navigation -->
      <div class="nav-links" :class="{ 'show': isMenuOpen }">
        <a href="#sobre-nosotros" class="nav-link" @click="closeMenu">{{ $t('options.us') }}</a>
        <a href="#beneficios" class="nav-link" @click="closeMenu">{{ $t('options.benefits') }}</a>
        <a href="#como-funciona" class="nav-link" @click="closeMenu">{{ $t('options.how') }}</a>
        <a href="#contacto" class="nav-link contact-btn" @click="closeMenu">{{ $t('options.contact') }}</a>
      </div>

      <!-- Hamburger Button -->
      <button class="hamburger" :class="{ 'is-active': isMenuOpen }" @click="toggleMenu" aria-label="Menu">
        <span class="hamburger-line"></span>
        <span class="hamburger-line"></span>
        <span class="hamburger-line"></span>
      </button>
    </nav>
  </header>
</template>

<style scoped>
header {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  z-index: 1000;
  background: rgba(255, 255, 255, 0.95);
  backdrop-filter: blur(10px);
  transition: all 0.3s ease;
  transform: translateY(0);
  height: 80px;
  display: flex;
  align-items: center;
  box-shadow: 0 2px 20px rgba(0, 0, 0, 0.1);
}

header.scrolled {
  background: rgba(255, 255, 255, 0.98);
  box-shadow: 0 5px 20px rgba(0, 0, 0, 0.15);
  height: 70px;
}

header.hidden {
  transform: translateY(-100%);
}

.nav-container {
  max-width: 1400px;
  margin: 0 auto;
  padding: 1rem 2rem;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.logo {
  display: flex;
  align-items: center;
  text-decoration: none;
  transition: transform 0.3s ease;
  z-index: 100;
  margin-right: 10px;
}

.logo:hover {
  transform: translateY(-2px);
}

.logo img {
  height: 40px;
  width: auto;
  object-fit: contain;
}

.nav-links {
  display: flex;
  gap: 2rem;
  align-items: center;
}

.nav-link {
  text-decoration: none;
  color: #333;
  font-weight: 500;
  font-size: 0.95rem;
  padding: 0.5rem 0;
  position: relative;
  transition: color 0.3s ease;
}

.nav-link::after {
  content: '';
  position: absolute;
  bottom: 0;
  left: 0;
  width: 0;
  height: 2px;
  background: var(--primary-blue);
  transition: width 0.3s ease;
}

.nav-link:hover {
  color: var(--primary-blue);
}

.nav-link:hover::after {
  width: 100%;
}

.contact-btn {
  background: var(--primary-blue);
  color: white !important;
  padding: 0.6rem 1.2rem;
  border-radius: 8px;
  transition: all 0.3s ease;
}

.contact-btn:hover {
  background: var(--primary-blue-dark);
  transform: translateY(-2px);
}

.contact-btn::after {
  display: none;
}

.hamburger {
  display: none;
  background: none;
  border: none;
  cursor: pointer;
  padding: 0.5rem;
  z-index: 100;
  position: relative;
}

.hamburger-line {
  display: block;
  width: 24px;
  height: 2px;
  background: #333;
  transition: all 0.3s ease;
  position: relative;
}

.hamburger-line + .hamburger-line {
  margin-top: 6px;
}

.hamburger.is-active .hamburger-line:nth-child(1) {
  transform: translateY(8px) rotate(45deg);
}

.hamburger.is-active .hamburger-line:nth-child(2) {
  opacity: 0;
}

.hamburger.is-active .hamburger-line:nth-child(3) {
  transform: translateY(-8px) rotate(-45deg);
}

@media (max-width: 768px) {
  header {
    height: 70px;
  }

  .nav-container {
    padding: 0 1rem;
    width: 100%;
  }

  .hamburger {
    display: block;
  }

  .nav-links {
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    height: 100vh;
    width: 100%;
    background: linear-gradient(135deg, var(--primary-blue) 0%, var(--primary-blue-dark) 100%);
    display: flex !important;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    padding: 80px 2rem 2rem 2rem;
    gap: 1.5rem;
    transform: translateX(100%);
    transition: transform 0.3s ease;
    z-index: 90;
    overflow-y: auto;
    box-shadow: -5px 0 20px rgba(0, 0, 0, 0.2);
  }

  .nav-links::before {
    display: none;
  }

  .nav-links.show {
    transform: translateX(0);
  }

  .nav-link {
    font-size: 1.2rem;
    text-align: center;
    width: 100%;
    max-width: 300px;
    color: white;
    padding: 1rem;
    background: rgba(255, 255, 255, 0.1);
    backdrop-filter: blur(10px);
    border: 1px solid rgba(255, 255, 255, 0.2);
    border-radius: 8px;
    margin: 0;
    transition: all 0.3s ease;
  }

  .nav-link:hover {
    background: rgba(255, 255, 255, 0.2);
    transform: translateY(-2px);
  }

  .contact-btn {
    width: auto;
    min-width: 200px;
    margin-top: 0.5rem;
    display: inline-block;
    background: white;
    color: var(--primary-blue) !important;
  }

  .contact-btn:hover {
    background: rgba(255, 255, 255, 0.9);
    transform: translateY(-2px);
  }

  .logo img {
    height: 35px;
  }

  .hamburger.is-active .hamburger-line {
    background: white;
  }
}
</style>

<style>
:root {
  --primary-blue-rgb: 51, 153, 255;
}
</style>