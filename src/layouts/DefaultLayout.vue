<script setup lang="ts">
import DefaultNav from '@/layouts/components/DefaultNav.vue'
// import BannerImg from '@/assets/images/banner.png'
</script>
<template>
  <div class="layout-wrapper">
    <DefaultNav />
    <div class="layout-content-wrapper">
      <!-- <img :src="BannerImg" class="layout-banner" /> -->
      <div class="layout-intro">
        <h1 class="layout-intro__title">白頭翁 (Chinese bulbul)</h1>
        <span class="layout-intro__description">
          又名白頭鵯。以果實、昆蟲為主食，無法消化小米、穀類。平均壽命約 8~10 年。
        </span>
      </div>
      <div class="page-wrapper">
        <RouterView />
      </div>
    </div>
  </div>
</template>
<style scoped lang="sass">
.layout-wrapper
  display: flex
  height: 100vh
  width: 100%

.layout-content-wrapper
  width: 100%
  display: flex
  flex-direction: column
  background-image: url(@/assets/images/banner.png)
  background-size: cover
  background-repeat: no-repeat
  background-position: 70% 40%
  padding-top: 500px

.layout-intro
  text-align: end
  padding-right: 44px
  padding-bottom: 36px
  color: white
  &__title
    margin-bottom: 4px
    font-weight: 700
    font-size: 48px
    line-height: 65px
  &__description
    font-size: 18px
    line-height: 24px

.page-wrapper
  height: 100%
  background-color: $background-primary

@media (max-width: $mobile)
  .layout-wrapper-inner
    max-width: 315px
    margin: 0 30px
</style>
