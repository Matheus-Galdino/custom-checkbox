<template>
  <div class="checkbox-container">
    <input type="checkbox" :id="id" :checked="modelValue" @input="$emit('update:modelValue', !modelValue)" hidden />
    <div class="checkbox" @click="$emit('update:modelValue', !modelValue)">
      <img src="../assets/check.svg" alt="" />
    </div>
    <label :for="id">{{ label }}</label>
  </div>
</template>

<script>
export default {
  name: "Checkbox",
  props: {
    modelValue: {
      type: Boolean,
      default: false,
    },
    id: {
      type: String,
      required: true,
    },
    label: {
      type: String,
      required: true,
    },
  },
};
</script>

<style>
.checkbox-container {
  display: flex;
  column-gap: 5px;
  align-items: center;
}

.checkbox {
  display: inline-grid;
  place-content: center;

  cursor: pointer;
  border-radius: 5px;
  border: 1px solid #f9a109;
}

.checkbox img {
  opacity: 0;
  visibility: hidden;
  transition: all 0.3s ease-in-out;
}

input:checked ~ .checkbox img {
  opacity: 1;
  visibility: visible;
}

label {
  cursor: pointer;
}
</style>
