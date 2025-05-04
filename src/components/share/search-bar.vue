<script setup>
import { ref } from 'vue';

const props = defineProps({
  placeholder: {
    type: String,
    default: 'Buscar...'
  }
});

const emit = defineEmits(['update:query']);

const searchQuery = ref('');

const emitSearch = () => {
  emit('update:query', searchQuery.value);
};

const clearSearch = () => {
  searchQuery.value = '';
  emitSearch();
};
</script>

<template>
  <div class="search-bar">
    <span class="p-input-icon-left w-full">
      <i class="pi pi-search" />
      <InputText
          v-model="searchQuery"
          :placeholder="placeholder"
          class="w-full"
          @keydown.enter="emitSearch"
      />
    </span>
    <Button
        icon="pi pi-times"
        class="p-button-text p-button-sm ml-2"
        v-if="searchQuery"
        @click="clearSearch"
    />
  </div>
</template>

<style scoped>
.search-bar {
  display: flex;
  align-items: center;
  max-width: 400px;
  margin: auto;
}
</style>