<script setup>
import ArrowIcon from '../icons/arrow.vue';
</script>

<template>
  <div class="info-section">
    <div class="container">
      <div class="info-section-text">
        <h1 class="info-section-text__title">{{ $t('home.infoSection.title') }}</h1>
        <span class="info-section-text__description">{{ $t('home.infoSection.description') }}</span>
        <div class="learn-more-link">
          <a href="/about">{{ $t('learnMore') }}</a>
          <ArrowIcon/>
        </div>
      </div>
      <div class="info-section-image">
        <img src="@/assets/images/home/info-section.png" alt="App Image">
      </div>
    </div>
  </div>
</template>

<script>

export default {
  name: 'HomeInfoSection',
  components: {
    ArrowIcon
  }
}

</script>

<style scoped>

.info-section {
  padding: 80px 0;
}

.info-section-text {
  max-width: 460px;
}

.info-section-text__title {
  color: var(--color-heading);
  font-size: 50px;
  font-style: normal;
  font-weight: 700;
  line-height: 64px;
  margin-bottom: 24px;
}

.info-section-text__description {
  color: var(--color-text);
  font-size: 18px;
  font-style: normal;
  font-weight: 400;
  line-height: 27px;
}

.info-section-image {
  margin-right: -150px;
}

.info-section-image img {
  transform: translate(265px, 0);
}

@media screen and (max-width: 820px) {
  .info-section-image {
    display: none;
  }
}
@media screen and (max-width: 480px) {
  .info-section-text__title{
    font-size: 36px;
  }
}

</style>