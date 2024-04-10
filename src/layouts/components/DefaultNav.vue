<script setup lang="ts"></script>
<template>
  <div class="nav-wrapper">
    <h3 class="nav-title">白頭翁不吃米</h3>
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
  flex-direction: column
  align-items: center
  justify-content: start
  box-shadow: 0px 4px 4px 0px $shadow

.nav-title
  margin-bottom: 75px
  font-weight: 700
  font-size: 30px
  line-height: 40px

.nav-href
  font-size: 18px
  line-height: 24px
  margin-bottom: 16px
  .active
    color: #AA6666
    text-decoration: underline
</style>
