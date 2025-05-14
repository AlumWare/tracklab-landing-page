<template>
  <footer class="footer">    
    <div class="footer__container">
      <div class="footer__section">
        <h3 class="footer__heading">{{ $t('footer.register') }}</h3>
        <button class="footer__button">{{ $t('footer.account') }}</button>
        <social-icons />
      </div>
      
      <div class="footer__section">
        <h3 class="footer__heading">Links</h3>
        <ul class="footer__links">
          <li><a href="#sobre-nosotros" class="footer__link">{{ $t('footer.us') }}</a></li>
          <li><a href="#beneficios" class="footer__link">{{ $t('footer.benefits') }}</a></li>
          <li><a href="#como-funciona" class="footer__link">{{ $t('footer.how') }}</a></li>
          <li><a href="#planes" class="footer__link">{{ $t('footer.plans') }}</a></li>
          <li><a href="#contacto" class="footer__link">{{ $t('footer.contact') }}</a></li>
          <li><a href="#preguntas-frecuentes" class="footer__link">FAQ</a></li>
        </ul>
      </div>
      
      <div class="footer__section">
        <h3 class="footer__heading">{{ $t('footer.contact') }}</h3>
        <div class="footer__contact">
          <div class="footer__contact-item">
            <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" viewBox="0 0 16 16">
              <path d="M.05 3.555A2 2 0 0 1 2 2h12a2 2 0 0 1 1.95 1.555L8 8.414.05 3.555ZM0 4.697v7.104l5.803-3.558L0 4.697ZM6.761 8.83l-6.57 4.027A2 2 0 0 0 2 14h12a2 2 0 0 0 1.808-1.144l-6.57-4.027L8 9.586l-1.239-.757Zm3.436-.586L16 11.801V4.697l-5.803 3.546Z"/>
            </svg>
            <span>TrackLab@gmail.com</span>
          </div>
          <div class="footer__contact-item">
            <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" viewBox="0 0 16 16">
              <path d="M1.885.511a1.745 1.745 0 0 1 2.61.163L6.29 2.98c.329.423.445.974.315 1.494l-.547 2.19a.678.678 0 0 0 .178.643l2.457 2.457a.678.678 0 0 0 .644.178l2.189-.547a1.745 1.745 0 0 1 1.494.315l2.306 1.794c.829.645.905 1.87.163 2.611l-1.034 1.034c-.74.74-1.846 1.065-2.877.702a18.634 18.634 0 0 1-7.01-4.42 18.634 18.634 0 0 1-4.42-7.009c-.362-1.03-.037-2.137.703-2.877L1.885.511z"/>
            </svg>
            <span>+51 956 518 291</span>
          </div>
        </div>
      </div>
      
      <div class="footer__section">
        <h3 class="footer__heading">Legal</h3>
        <ul class="footer__links">
          <li><a href="#" class="footer__link">{{ $t('footer.politics') }}</a></li>
          <li><a href="#" class="footer__link">{{ $t('footer.terms') }}</a></li>
        </ul>
      </div>
    </div>
  </footer>
</template>

<script>
import SocialIcons from '../share/social-icons.vue';

export default {
  name: 'Footer',
  components: {
    SocialIcons
  }
}
</script>

<style scoped>
.footer {
  position: relative;
  background-color: #18558F;
  color: white;
  padding: 3rem 1rem;
  overflow: hidden;
}

.footer__background {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  z-index: 0;
}

.footer__container {
  position: relative;
  z-index: 1;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  max-width: 1200px;
  margin: 0 auto;
}

.footer__section {
  flex: 1 1 200px;
  margin: 1rem;
}

.footer__heading {
  font-size: 1.25rem;
  font-weight: 600;
  margin-bottom: 1.5rem;
}

.footer__button {
  background-color: white;
  color: #18558F;
  border: none;
  border-radius: 100px;
  padding: 0.75rem 1.5rem;
  font-weight: 600;
  cursor: pointer;
  transition: background-color 0.2s ease;
  margin-bottom: 1.5rem;
}

.footer__button:hover {
  background-color: #f0f0f0;
}

.footer__links {
  list-style: none;
  padding: 0;
  margin: 0;
}

.footer__links li {
  margin-bottom: 1rem;
}

.footer__link {
  color: white;
  text-decoration: none;
  transition: color 0.2s ease;
}

.footer__link:hover {
  color: #ccc;
}

.footer__contact-item {
  display: flex;
  align-items: center;
  margin-bottom: 1rem;
}

.footer__contact-item svg {
  margin-right: 0.75rem;
}

@media (max-width: 768px) {
  .footer__container {
    flex-direction: column;
  }
  
  .footer__section {
    margin: 1rem 0;
  }
}
</style>
