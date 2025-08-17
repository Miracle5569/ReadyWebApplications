<script setup lang="ts">
import SeeApplicationButton from './SeeApplicationButton.vue'
</script>

<template>
  <main class="content">
    <section class="section container">
      <header class="section__header">
        <h2 class="section__title">Готовые веб-приложения, которые вы можете настроить</h2>
      </header>
      <div class="section__body">
        <div class="look">
          <div class="look__info">
            <div class="look__description">
              Покупайте готовые веб-приложения и редактируйте их под свои нужды
            </div>
            <SeeApplicationButton />
          </div>
          <img
            src="../../src/images/interface-control-svgrepo-com.svg"
            alt="Look Applications"
            class="look__image"
            width="450"
            height="200"
            loading="lazy"
          />
        </div>
      </div>
    </section>
  </main>
</template>

<style scoped lang="scss">
.content {
  background-color: rgba(237, 246, 254, 255);
  padding-block: 60px;
}

.section {
  &__title {
    font-size: 80px;
    line-height: 85px;
    font-weight: 400;
  }
}

.look {
  display: flex;
  align-items: center;
  justify-content: space-between;

  &__info {
    width: 50%;
    height: 230px;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
  }

  &__description {
    font-size: 35px;
    font-weight: 400;
  }
}
</style>
