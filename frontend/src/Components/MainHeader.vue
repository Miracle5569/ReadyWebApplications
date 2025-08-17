<script setup lang="ts"></script>

<template>
  <div class="header">
    <div class="header__inner container">
      <span class="header__logo">Готовые веб-приложения</span>
      <nav class="header__menu">
        <ul class="header__menu-list">
          <li class="header__menu-item">Вход</li>
          <li class="header__menu-item">Регистрация</li>
        </ul>
      </nav>
    </div>
  </div>
</template>

<style scoped lang="scss">
@use '../style/abstracts/media' as media;

.header {
  padding-block: 20px;

  &__inner {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  &__logo {
    font-size: 20px;
    // font-weight: 600;
  }

  &__menu {
    &-list {
      display: inline-flex;
      justify-content: space-between;
      align-items: center;
      width: 200px;
    }

    &-item {
      padding: 5px 10px;

      @include media.hover {
        border-radius: 20px;
        background-color: rgba(236, 246, 254, 255);
        cursor: pointer;
      }
    }
  }
}
</style>
