<script setup lang="ts">
import { ref } from 'vue'
import { useDevice } from '@/hook/device'

import LogoButton from '@/layouts/components/LogoButton.vue'
import HamburgerButton from '@/layouts/components/HamburgerButton.vue'

const { deviceType } = useDevice()

const isExpanded = ref(false)

const handleHamburgerClick = () => {
  isExpanded.value = !isExpanded.value
}
</script>
<template>
  <div class="nav-wrapper">
    <HamburgerButton v-if="deviceType === 'mobile'" @click="handleHamburgerClick" />
    <h3 class="nav-title">白頭翁不吃米</h3>
    <RouterLink class="logo-button" to="/">
      <LogoButton />
    </RouterLink>
    <div class="nav-href-wrapper" v-if="deviceType !== 'mobile'">
      <RouterLink class="nav-href active" to="/"> 白頭翁的特性</RouterLink>
      <RouterLink class="nav-href" to="/"> 白頭翁的故事</RouterLink>
      <RouterLink class="nav-href" to="/"> 白頭翁的美照</RouterLink>
      <RouterLink class="nav-href" to="/"> 白頭翁的危機</RouterLink>
    </div>
  </div>
  <div
    class="nav-href-wrapper"
    v-if="deviceType === 'mobile'"
    :class="isExpanded ? 'expanded' : ''"
  >
    <RouterLink class="nav-href active" to="/"> 白頭翁的特性</RouterLink>
    <RouterLink class="nav-href" to="/"> 白頭翁的故事</RouterLink>
    <RouterLink class="nav-href" to="/"> 白頭翁的美照</RouterLink>
    <RouterLink class="nav-href" to="/"> 白頭翁的危機</RouterLink>
  </div>
</template>
<style scoped lang="sass">
.nav-wrapper
  width: 345px
  height: 100%
  padding-top: 78px
  box-sizing: border-box
  display: flex
  flex-shrink: 0
  flex-direction: column
  align-items: center
  justify-content: start
  box-shadow: 0px 4px 4px 0px $shadow
  position: relative

.nav-title
  margin-top: 0
  margin-bottom: 75px
  font-weight: 700
  font-size: 30px
  line-height: 40px

.nav-href-wrapper
  display: flex
  flex-direction: column
  align-items: center

.nav-href
  font-size: 18px
  line-height: 24px
  margin-bottom: 16px
  &.active
    color: #AA6666
    text-decoration: underline

.logo-button
  position: absolute
  top: 47px
  right: -50px

@media (max-width: $mobile)
  .nav-wrapper
    flex-direction: row
    width: 100%
    height: unset
    position: sticky
    justify-content: space-between
    padding: 20px 18px

  .nav-title
    font-size: 20px
    line-height: 27px
    margin: 0

  .logo-button
    position: unset

  .nav-href-wrapper
    display: none
    &.expanded
      display: flex
</style>
