<script setup lang="ts"></script>

<template>
  <button class="see-application">Посмотреть приложения</button>
</template>

<style scoped lang="scss">
@use '../style/abstracts/mixins' as *;
@use '../style/abstracts/media' as media;

.see-application {
  @include reset-button;

  max-width: 80%;
  height: 90px;
  color: white;
  background-color: rgba(50, 108, 225, 255);
  border-radius: 10px;
  font-size: 30px;

  @include media.hover {
    opacity: 0.8;
  }
}
</style>
