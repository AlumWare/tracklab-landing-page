<template>
  <div class="extension-panel">
    <div 
      class="extension-panel__header" 
      @click="isOpen = !isOpen"
      :class="{ 'extension-panel__header--active': isOpen }"
    >
      <h3 class="extension-panel__title">{{ title }}</h3>
      <span class="extension-panel__icon">
        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="feather feather-chevron-down" :class="{ 'rotate-icon': isOpen }">
          <polyline points="6 9 12 15 18 9"></polyline>
        </svg>
      </span>
    </div>
    <div class="extension-panel__content-container" :class="{ 'extension-panel__content-container--open': isOpen }">
      <div class="extension-panel__content">
        <div v-if="htmlContent" v-html="htmlContent"></div>
        <slot v-else></slot>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ExtensionPanel',
  props: {
    title: {
      type: String,
      required: true
    },
    htmlContent: {
      type: String,
      default: null
    },
    initiallyOpen: {
      type: Boolean,
      default: false
    }
  },
  data() {
    return {
      isOpen: this.initiallyOpen
    }
  }
}
</script>

<style scoped>
.extension-panel {
  border: 1px solid #e2e8f0;
  border-radius: 0.5rem;
  margin-bottom: 1rem;
  background-color: white;
  box-shadow: 0 1px 3px 0 rgba(0, 0, 0, 0.1), 0 1px 2px 0 rgba(0, 0, 0, 0.06);
  overflow: hidden;
}

.extension-panel__header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1rem 1.5rem;
  cursor: pointer;
  transition: background-color 0.2s ease;
}

.extension-panel__header:hover {
  background-color: #f7fafc;
}

.extension-panel__header--active {
  background-color: #f7fafc;
}

.extension-panel__title {
  margin: 0;
  font-size: 1rem;
  font-weight: 500;
  color: #2d3748;
}

.extension-panel__icon {
  color: #000;
  display: flex;
  align-items: center;
}

.extension-panel__icon svg {
  width: 1.25rem;
  height: 1.25rem;
  transition: transform 0.25s ease-in-out;
}

.rotate-icon {
  transform: rotate(180deg);
}

.extension-panel__content-container {
  max-height: 0;
  overflow: hidden;
  transition: max-height 0.3s ease-in-out;
  border-top: 0px solid #e2e8f0;
}

.extension-panel__content-container--open {
  max-height: 1000px;
  border-top: 1px solid #e2e8f0;
}

.extension-panel__content {
  padding: 0;
  color: #4a5568;
  font-size: 0.95rem;
  line-height: 1.5;
  opacity: 0;
  transition: opacity 0.25s ease, padding 0.25s ease;
}

.extension-panel__content-container--open .extension-panel__content {
  padding: 1rem 1.5rem;
  opacity: 1;
}

.extension-panel__content p {
  margin-bottom: 0.75rem;
  color: #4a5568;
}

.extension-panel__content p:last-child {
  margin-bottom: 0;
}
</style>
