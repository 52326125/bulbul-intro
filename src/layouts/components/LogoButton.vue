<script setup lang="ts">
defineEmits(['click'])
</script>
<template>
  <button class="logo-button-wrapper" @click="$emit('click')">
    <div class="logo-button-inner__shape">
      <div class="logo-button-inner__fill" />
      <div class="logo-button-inner__beak" />
    </div>
  </button>
</template>
<style scoped lang="sass">
.logo-button-wrapper
  border-radius: 50%
  box-shadow: 0px 0px 6px 0px $shadow
  width: 97px
  height: 97px
  position: relative
  display: flex
  align-items: center
  justify-content: center
  background: white
  border: none

.logo-button-inner__shape
  background-color: black
  border-radius: 50%
  width: 55%
  height: 45%
  position: relative
  &::after
    display: block
    content: ''
    background: black
    width: 75%
    height: 16%
    position: relative
    bottom: 5%
    border-radius: 0 0 70% 0

.logo-button-inner__fill
  background: white
  border-radius: 50%
  width: 100%
  height: 80%
  margin-top: 8%
  transform: rotate(-15deg)
  position: relative
  &::after
    display: block
    content: ''
    background: black
    border-radius: 50%
    width: 10px
    height: 10px
    position: absolute
    right: 15%
    top: 30%

.logo-button-inner__beak
  background: black
  width: 10px
  height: 5px
  position: absolute
  top: 10px
  right: -10px
  border-radius: 0 90% 0 0
  transform: rotate(-10deg)

@media (max-width: $mobile)
  .logo-button-wrapper
    width: 48px
    height: 48px
    position: relative

  .logo-button-inner__fill
    &::after
      width: 5px
      height: 5px

  .logo-button-inner__beak
    width: 5px
    height: 3px
    top: 5px
    right: -5px
</style>
