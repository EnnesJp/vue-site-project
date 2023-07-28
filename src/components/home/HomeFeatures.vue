<script setup>
import ArrowIcon from '../icons/arrow.vue';
</script>

<template>
  <div class="container">
    <div
      class="feature-section"
      v-for="(feature, index) in getFeatures"
      :key="index">
      <img class="feature-section__image" :src="`src/assets/images/home/${feature.icon}`" alt="Feature Image">
      <div class="feature-section-info">
        <h2 class="feature-section-info__title">{{ feature.title }}</h2>
        <p class="feature-section-info__text">{{ feature.text }}</p>
        <div class="learn-more-link">
          <a href="/about">Learn more</a>
          <ArrowIcon/>
        </div>
      </div>
    </div>
  </div>
</template>

<script>

export default {
  name: 'HomeFeatures',
  components: {
    ArrowIcon
  },
  computed: {
    getFeatures() {
      const features = [
        {
          title: this.$t('home.features.1.title'),
          text: this.$t('home.features.1.text'),
          icon: 'features1.png',
        },
        {
          title: this.$t('home.features.2.title'),
          text: this.$t('home.features.2.text'),
          icon: 'features2.png',
        },
        {
          title: this.$t('home.features.3.title'),
          text: this.$t('home.features.3.text'),
          icon: 'features3.png',
        },
      ];

      return features;
    }
  }
}

</script>

<style scoped>

.container {
  flex-direction: column;
}

.feature-section {
  display: flex;
  padding: 80px 0;
  align-items: center;
  gap: 139px;
}

.feature-section:nth-child(even) {
  flex-direction: row-reverse;
}

.feature-section__image {
  max-width: 565px;
  max-height: 565px;

}
.feature-section-info {
  max-width: 565px;
}

.feature-section-info__title {
  color: var(--color-heading);
  font-size: 50px;
  font-style: normal;
  font-weight: 700;
  line-height: 64px;
  margin-bottom: 24px;
}

.feature-section-info__text {
  color: var(--color-text);
  font-size: 18px;
  font-style: normal;
  font-weight: 400;
  line-height: 27px;
  margin-bottom: 51px;
}

@media screen and (max-width: 820px) {
  .feature-section {
    flex-direction: column;
  }
  .feature-section:nth-child(even) {
    flex-direction: column;
  }
}

@media screen and (max-width: 480px) {
  .feature-section {
    gap: 80px;
  }
  .feature-section__image {
    max-width: 360px;
    max-height: 360px;
  }
  .feature-section-info__title {
    font-size: 36px
  }
}

</style>