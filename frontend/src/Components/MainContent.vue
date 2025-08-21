<script setup lang="ts">
import { ref } from 'vue'
import ApplicationButton from './ApplicationButton.vue'
import ApplicationItem from './ApplicationItem.vue'

// Вынести куда-нибудь( на подумать )
const applicationsItems = ref([
  {
    picture: '/icons/conversation-svgrepo-com (1).svg',
    headerText: 'E-commerce',
    description:
      'Запустите свой интернет-магазин с помощью наших готовых приложений для электронной коммерции',
  },

  {
    picture: '/icons/calendar-svgrepo-com (1).svg',
    headerText: 'Система бронирования',
    description:
      'Управляйте бронированием и записью на прием с помощью наших готовых систем бронирования',
  },
  {
    picture: '/icons/user-svgrepo-com (1).svg',
    headerText: 'CRM',
    description:
      'Управляйте взаимоотношениями с клиентами и продажами с помощью наших готовых CRM-приложений',
  },
  {
    picture: '/icons/creativity-svgrepo-com (1).svg',
    headerText: 'Управление обучением',
    description: 'Запускайте свои онлайн-курсы с помощью наших готовых систем управления обучением',
  },
])
</script>

<template>
  <main class="content">
    <section class="section container">
      <header class="section__header">
        <div class="section__header-info">
          <h2 class="section__title">Готовые к использованию веб-приложения</h2>
          <p class="section__decription">
            Быстро запустите свой проект с помощью готовых к использованию веб-приложений
          </p>
          <ApplicationButton :text="'Попробовать сейчас'" :btn-padding="'20px 50px'" />
        </div>
        <img
          src="../images/undraw_designer_efwz.svg"
          alt="Попробовать сейчас"
          class="section__image"
          loading="lazy"
          width="570"
          height="285"
        />
      </header>

      <div class="section__body">
        <div class="applications">
          <h4 class="applications__featured">Рекомендованные приложения</h4>
          <ul class="applications__list">
            <ApplicationItem
              v-for="(item, index) in applicationsItems"
              :key="index"
              :picture="item.picture"
              :header-text="item.headerText"
              :description="item.description"
            />
          </ul>
        </div>
      </div>
    </section>

    <section class="section-free container">
      <header class="section-free__header">
        <h3 class="section-free__title">Начните бесплатно</h3>
        <p class="section-free__description">
          Откройте для себя преимущества нашей платформы, начав бесплатную пробную версию уже
          сегодня.
        </p>
      </header>

      <div class="section-free__body">
        <ApplicationButton :text="'Начать'" :btn-padding="'17px 60px'" />
      </div>
    </section>
  </main>
</template>

<style scoped lang="scss">
.content {
  padding-block: 95px;
}

.section {
  &__header {
    display: flex;

    &-info {
      & > *:not(:last-child) {
        margin-bottom: 40px;
      }
    }
  }

  &__body {
    margin-top: 75px;
  }

  &__title {
    font-size: 50px;
  }

  &__decription {
    font-size: 25px;
  }
}

.applications {
  &__featured {
    font-size: 30px;
    margin-bottom: 30px;
  }

  &__list {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 30px;
  }

  &__item {
    border: var(--border);
    display: inline-flex;
    padding: 40px 20px;
  }
}

.section-free {
  display: flex;
  align-self: center;
  justify-content: space-between;
  padding-top: 80px;

  &__title {
    margin-bottom: 20px;
  }

  &__description {
    font-size: 20px;
  }

  &__body {
    margin-block: auto;
  }
}
</style>
