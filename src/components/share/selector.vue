<script setup>
import { ref, watch } from 'vue';

const props = defineProps({
  options: {
    type: Array,
    required: true
  },
  modelValue: {
    type: [String, Number, Object, null],
    default: null
  },
  placeholder: {
    type: String,
    default: 'Seleccionar...'
  },
  optionLabel: {
    type: String,
    default: 'label' // el nombre del campo que se mostrará
  }
});

const emit = defineEmits(['update:modelValue']);

const selected = ref(props.modelValue);

watch(() => props.modelValue, (newVal) => {
  selected.value = newVal;
});

const emitSelection = () => {
  emit('update:modelValue', selected.value);
};
</script>

<template>
  <div class="selector-wrapper">
    <Dropdown
        v-model="selected"
        :options="options"
        :optionLabel="optionLabel"
        :placeholder="placeholder"
        class="w-full"
        @change="emitSelection"
    />
  </div>
</template>

<style scoped>
.selector-wrapper {
  max-width: 400px;
  margin: auto;
}
</style>