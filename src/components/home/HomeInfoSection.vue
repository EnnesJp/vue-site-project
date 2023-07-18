<script setup>
import ArrowIcon from '../icons/arrow.vue';
</script>

<template>
  <div class="info-section">
    <div class="container">
      <div class="info-section-text">
        <h1 class="info-section-text__title">Chats for your distributed teams</h1>
        <span class="info-section-text__description">Team combines the immediacy of real-time chat with an email threading model. With Team, you can catch up on important conversations while ignoring irrelevant ones.</span>
        <div class="learn-more-link">
          <a href="/about">Learn more</a>
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
  transform: translate(250px, 0);
}

</style>