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
          title: 'Chats for your distributed teams',
          text: 'Team combines the immediacy of real-time chat with an email threading model. With Team, you can catch up on important conversations while ignoring irrelevant ones.',
          icon: 'features1.png',
        },
        {
          title: 'Choose how you want to work',
          text: 'In Team, you’ve got all the flexibility to work when, where and how it’s best for you. You can easily chat, send audio and video clips, or hop on a huddle to talk things out live.',
          icon: 'features2.png',
        },
        {
          title: 'Move faster with your Team tools',
          text: 'With your other work apps connected to Team, you can work faster by switching tabs less. And with powerful tools like Workflow Builder, you can automate away routine tasks..',
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

</style>