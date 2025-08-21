<script setup lang="ts">
interface Props {
  headerText: string
  description: string
  picture: string
}

const props = defineProps<Props>()
</script>

<template>
  <li class="application__item">
    <img
      class="application__image"
      width="70"
      height="35"
      :src="props.picture"
      :alt="props.headerText"
      loading="lazy"
    />
    <div class="application__info">
      <div class="application__info-text">{{ props.headerText }}</div>
      <div class="application__info-description">{{ props.description }}</div>
      <a class="application__info-more" href="/"
        >Посмотреть дитали
        <img
          width="40"
          height="20"
          class="application__more-image"
          src="/icons/arrow-right-svgrepo-com (5).svg"
          alt="Посмотреть детали"
          loading="lazy"
      /></a>
    </div>
  </li>
</template>

<style scoped lang="scss">
@use '../style/abstracts/mixins' as mix;
@use '../style/abstracts//media' as media;

.application__item {
  display: flex;
  align-items: flex-start;
  padding: 35px 25px;
  border-radius: 10px;
  -webkit-box-shadow: 0px 1px 33px -19px rgba(34, 60, 80, 0.2);
  -moz-box-shadow: 0px 1px 33px -19px rgba(34, 60, 80, 0.2);
  box-shadow: 0px 1px 33px -19px rgba(34, 60, 80, 0.2);

  & > :first-child {
    margin-right: 35px;
  }
}

.application__info {
  &-text {
    font-weight: 700;
    font-size: 22px;
    margin-bottom: 15px;
  }

  &-description {
    margin-bottom: 20px;
  }

  &-more {
    @include mix.reset-link;
    @include media.hover {
      opacity: 0.8;
    }

    & {
      display: flex;
      align-items: center;

      color: #6963ed;
    }
  }
}

.application__more-image {
  padding-top: 3px;
  margin-left: -4px;
}
</style>
