<script setup lang="ts">
defineEmits(['click'])
</script>
<template>
  <button class="hamburger-button-wrapper" @click="$emit('click')">
    <div class="hamburger-button-line" />
    <div class="hamburger-button-line short" />
    <div class="hamburger-button-line" />
  </button>
</template>
<style scoped lang="sass">
.hamburger-button-wrapper
  background: white
  border: none
  width: 24px
  display: flex
  flex-direction: column
  gap: 4px

.hamburger-button-line
  border: 2px solid black
  width: 100%
  &.short
    width: 50%
</style>
