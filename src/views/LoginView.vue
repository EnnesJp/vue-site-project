<template>
  <div class="login">
    <div class="container">
      <div class="login-wrapper">
        <form class="login-form">
          <h1 class="login-form__title">{{ $t('login.title') }}</h1>
          <p class="login-form__subtitle">{{ $t('login.description') }}</p>
          <div class="login-form-input">
            <span class="login-form-input__label">{{ $t('login.email') }}</span>
            <input type="text" class="login-form-input__username">
          </div>
          <div class="login-form-input">
            <span class="login-form-input__label">{{ $t('login.password') }}</span>
            <input type="password" class="login-form-input__password">
          </div>
          <a class="login-form__forget-password">{{ $t('login.forgotPassword') }}</a>
          <button type="submit" class="login-form__button btn btn-primary">
            {{ $t('login.login') }}
          </button>
        </form>
        <div class="login-alternative">
          {{ $t('login.alternative') }}
        </div>
        <div class="register__button btn btn-alternative">
          <RouterLink to="/register">{{ $t('login.register') }}</RouterLink>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
</script>

<style type="scss" scoped>
.login {
  margin-top: 132px;
  min-height: 580px;
}

.container {
  flex-direction: column;
}

.login-wrapper {
  width: 100vw;
  max-width: 420px;
  margin: 30px auto;
}

.login-form {
  display: flex;
  flex-direction: column;
  justify-content: center;
  gap: 24px;
}

.login-form__title {
  color: var(--color-heading);
  font-size: 28px;
  line-height: 30px;
  text-align: left;
  margin-bottom: 8px;
}

.login-form__subtitle {
  font-size: 14px;
  line-height: 21px;
  font-weight: 400;
  text-align: left;
  color: var(--color-heading);
  margin-bottom: 24px;
}

.login-form__forget-password {
  color: var(--color-link);
  text-align: right;
  font-size: 14px;
  font-weight: 500;
  margin-bottom: 12px;
}

.login-form-input {
  display: flex;
  flex-direction: column;
  gap: 8px;
}

.login-form-input__label {
  color: var(--color-text);
  text-align: left;
  font-weight: 400;
  font-size: 14px;
  display: block;
}

.login-form__button  {
  border: none;
  color: var(--color-nav-text);
  font-size: 18px;
  font-style: normal;
  font-weight: 600;
  line-height: 150%;
}

.login-alternative {
  color: var(--color-text);
  margin: 10px 0;
  width: 100%;
  display: grid;
  grid-template-columns: 1fr max-content 1fr;
  grid-column-gap: 20px;
  align-items: center;
  font-size: 14px;
}

.login-alternative::before {
  background-color: var(--color-text);
  content: "";
  height: 2px;
  display: block;
}

.login-alternative::after {
  background-color: var(--color-text);
  content: "";
  height: 2px;
  display: block;
}

.register__button {
  width: 100%;
  font-size: 18px;
  font-style: normal;
  font-weight: 600;
  line-height: 150%;
}

</style>