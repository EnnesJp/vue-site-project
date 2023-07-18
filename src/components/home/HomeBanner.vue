<template>
  <div class="banner">
    <div class="container">
      <div class="banner-info">
        <h1 class="banner-info__title">Instant collaboration for remote teams</h1>
        <span class="banner-info__description">All-in-one place for your remote team to chat, collaborate and track project progress.</span>
        <div class="banner-info-register">
          <input class="banner-info-register__input" type="email" placeholder="Email">
          <div class="btn btn-secondary">
            <RouterLink to="/register">Get Early Access</RouterLink>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>

.banner {
  background-image: url(@/assets/images/home/banner.png);
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center;
  height: 800px;
  width: 100vw;
  padding: 250px 0;
}

.banner-info {
  display: flex;
  flex-direction: column;
  gap: 16px;
  max-width: 560px;
}

.banner-info__title {
  color: var(--color-text-white);
  font-size: 50px;
  font-style: normal;
  font-weight: 700;
  line-height: 64px;
}

.banner-info__description {
  color: var(--color-text-white);
  font-size: 18px;
  font-style: normal;
  font-weight: 400;
  line-height: 27px;
  max-width: 397px;
}

.banner-info-register {
  display: flex;
  gap: 16px;
}

.banner-info-register__input{
  width: 298px;
}

</style>