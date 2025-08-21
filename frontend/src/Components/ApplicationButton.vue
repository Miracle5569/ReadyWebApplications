<script setup lang="ts">
interface applicationButton {
  text: string
  btnPadding: string
}

const props = defineProps<applicationButton>()
</script>

<template>
  <button class="see-application" :style="{ padding: props.btnPadding }">
    {{ props.text }}
  </button>
</template>

<style scoped lang="scss">
@use '../style/abstracts/mixins' as *;
@use '../style/abstracts/media' as media;

.see-application {
  @include reset-button;

  color: white;
  background-color: #6a63f6;
  border-radius: 10px;
  font-size: 20px;

  @include media.hover {
    opacity: 0.8;
  }
}
</style>
