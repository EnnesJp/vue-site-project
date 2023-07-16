<script setup>
import ArrowIcon from '../icons/arrow.vue';
</script>

<template>
  <div class="container">
    <div class="info-section">
      <h1 class="info-section-title">Chats for your distributed teams</h1>
      <span class="info-section-description">Team combines the immediacy of real-time chat with an email threading model. With Team, you can catch up on important conversations while ignoring irrelevant ones.</span>
      <div class="info-section-link">
        <a href="/about">Learn more</a>
        <ArrowIcon/>
      </div>
    </div>
    <img src="@/assets/images/home/info-section.png" alt="App Image">
  </div>
</template>

<style scoped>

.container {
  display: flex;
  padding: 80px 0 80px 140px;
  justify-content: flex-end;
  align-items: center;
  flex-shrink: 0;
}

.container .info-section {
  max-width: 460px;
}

.container .info-section .info-section-title {
  color: var(--color-heading);
  font-size: 50px;
  font-style: normal;
  font-weight: 700;
  line-height: 64px;
  margin-bottom: 24px;
}

.container .info-section .info-section-description {
  color: var(--color-text);
  font-family: Lexend Deca;
  font-size: 18px;
  font-style: normal;
  font-weight: 400;
  line-height: 27px;
}

.container .info-section .info-section-link {
  margin-top: 46px;
  display: flex;
  gap: 8px;
  align-items: center;
}

.container .info-section .info-section-link a {
  color: var(--color-link);
  font-size: 16px;
  font-style: normal;
  font-weight: 500;
  line-height: 150%;
}

</style>