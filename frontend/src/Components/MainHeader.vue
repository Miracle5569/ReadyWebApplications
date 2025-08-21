<script setup lang="ts"></script>

<template>
  <div class="header">
    <div class="header__inner container">
      <a class="header__logo" href="/">
        <img
          class="header__image"
          src="/icons/check-mark-svgrepo-com.svg"
          alt="Complete Web-Applications"
          loading="lazy"
          width="30"
          height="15"
        />
      </a>
      <nav class="header__menu">
        <ul class="header__menu-list">
          <li class="header__menu-item">Домой</li>
          <li class="header__menu-item">Каталог приложений</li>
          <li class="header__menu-item">О нас</li>
          <li class="header__menu-item">Контакты</li>
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
  }

  &__menu {
    &-list {
      display: inline-flex;
      justify-content: space-between;
      align-items: center;
    }

    &-item {
      padding: 5px 10px;
      margin-right: 29px;

      &:not(:last-child) {
        margin-right: 10px;
      }

      @include media.hover {
        border-radius: 20px;
        background-color: rgba(236, 246, 254, 255);
        cursor: pointer;
      }
    }
  }
}
</style>
