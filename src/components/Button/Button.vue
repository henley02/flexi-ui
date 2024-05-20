<template>
  <button
    class="fu-button"
    :class="{
      [`fu-button--${type}`]: type,
      [`fu-button--${size}`]: size,
      'is-plain': plain,
      'is-round': round,
      'is-circle': circle,
      'is-disabled': disabled,
    }"
    :disabled="disabled"
  >
    <span>
      <slot />
    </span>
  </button>
</template>

<script setup lang="ts">
import { defineOptions } from 'vue'
import type { ButtonProps } from './types'

defineOptions({
  name: 'FuButton'
})

defineProps<ButtonProps>()

</script>

<style scoped>

</style>