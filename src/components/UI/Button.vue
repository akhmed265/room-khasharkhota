<template>
  <button 
    :class="['button', `button--${variant}`]"
    :type="type"
    @click="$emit('click', $event)"
  >
    <slot></slot>
  </button>
</template>

<script setup lang="ts">
interface Props {
  variant?: 'dark-to-light' | 'light-to-dark'
  type?: 'button' | 'submit' | 'reset'
}

withDefaults(defineProps<Props>(), {
  variant: 'dark-to-light',
  type: 'button'
})

defineEmits<{
  click: [event: MouseEvent]
}>()
</script>

<style lang="scss" scoped>
@import "../../styles/variables.scss";
.button {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  border: 2px;
  background-color: $green-color;
  border-radius: 4px;
  cursor: pointer;
  font-family: Nunito Sans;
  font-weight: 600;
  transition: all 0.3s ease;
  padding: 16px 24px;
  font-size: $font-input;
  line-height: 1;
  outline: none;

  // Темный → Светлый при наведении
  &--dark-to-light {
    background-color: $green-color;
    color: $secondary-color;
    border: 1px solid $green-color;

    &:hover {
      background-color: $secondary-color;
      color: $green-color;
    }

    &:focus {
      background-color: $secondary-color;
      color: $green-color;
    }
  }

  // Светлый → Темный при наведении
  &--light-to-dark {
    background-color: $secondary-color;
    color: $green-color;
    border: 1px solid $secondary-color;

    &:hover {
      background-color: $green-color;
      color: $secondary-color;
    }

    &:focus {
      background-color: $green-color;
      color: $secondary-color;
    }
  }

  // Состояния
  &:disabled {
    opacity: 0.6;
    cursor: not-allowed;
  }
}
</style>