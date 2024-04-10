<script setup lang="ts">
interface DescriptionBlockProps {
  title: string
  description: string
}

defineProps<DescriptionBlockProps>()
</script>
<template>
  <div class="description-block-wrapper">
    <h1 class="description-block-title">{{ title }}</h1>
    <p class="description-block-description">{{ description }}</p>
  </div>
</template>
<style scoped lang="sass">
.description-block-wrapper
  display: flex
  align-items: start
  gap: 36px
  max-width: 278px

.description-block-title
  position: relative
  margin: 0
  font-weight: 700
  font-size: 36px
  line-height: 40px
  &::after
    display: block
    content: ''
    position: absolute
    box-sizing: border-box
    width: 25px
    height: 25px
    border: 8px solid #AA666699
    border-radius: 50%
    right: -10px
    bottom: -10px

.description-block-description
  margin: 0
</style>
