<script setup lang="ts">
import MainContent from './Components/MainContent.vue'
import MainHeader from './Components/MainHeader.vue'
</script>

<template>
  <div id="app">
    <MainHeader />
    <MainContent />
  </div>
</template>

<style scoped lang="scss">
#app {
  font-size: 18px;
  font-family: 'Ubuntu';
}
</style>
