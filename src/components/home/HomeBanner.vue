<template>
  <div class="container">
    <div class="banner-info">
      <h1 class="banner-info-title">Instant collaboration for remote teams</h1>
      <span class="banner-info-description">All-in-one place for your remote team to chat, collaborate and track project progress.</span>
      <div class="banner-register">
        <input class="banner-register-input" type="email" placeholder="Email">
        <div class="btn btn-secondary">
          <RouterLink to="/register">Get Early Access</RouterLink>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>

.container {
  background-image: url(@/assets/images/home/banner.png);
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center;
  height: 100vh;
  width: 100vw;
  padding: 250px;
}

.container .banner-info {
  display: flex;
  flex-direction: column;
  gap: 16px;
  max-width: 560px;
}

.container .banner-info .banner-info-title {
  color: var(--color-text-banner);
  font-size: 50px;
  font-style: normal;
  font-weight: 700;
  line-height: 64px;
}

.container .banner-info .banner-info-description {
  color: var(--color-text-banner);
  font-size: 18px;
  font-style: normal;
  font-weight: 400;
  line-height: 27px;
  max-width: 397px;
}

.container .banner-info .banner-register {
  display: flex;
  gap: 16px;
}

.container .banner-info .banner-register .banner-register-input{
  width: 298px;
}

</style>