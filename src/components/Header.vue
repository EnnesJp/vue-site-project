<script setup>
import SelectLang from './shared/SelectLang.vue';
</script>

<template>
  <div :class="isFilled ? 'header filled' : 'header'">
    <div class="container">
      <img src="@/assets/images/logo.png" class="header__logo" alt="Logo" @click="$router.push('/')">
      <div class="navbar">
        <RouterLink class="navbar__link" to="/products">{{ $t('nav.products') }}</RouterLink>
        <RouterLink class="navbar__link" to="/blog">{{ $t('nav.blog') }}</RouterLink>
        <RouterLink class="navbar__link" to="/support">{{ $t('nav.support') }}</RouterLink>
        <RouterLink class="navbar__link" to="/login">{{ $t('nav.login') }}</RouterLink>
        <div class="btn btn-primary">
          <RouterLink to="/register">{{ $t('nav.register') }}</RouterLink>
        </div>
      </div>
      <SelectLang/>
    </div>
  </div>
</template>

<script>

export default {
  name: 'Header',
  computed: {
    isFilled() {
      return this.$route.meta.filledMenu;
    }
  }
}

</script>

<style scoped>

.header {
  position: absolute;
  top: 0;
  width: 100vw;
  padding: 40px 0;
}

.header__logo {
  cursor: pointer;
}

.filled {
  background-color: var(--color-background-header);
}

.container {
  position: relative;
}

.navbar {
  display: flex;
  justify-content: flex-end;
  align-items: center;
  width: 100%;
  padding-right: 20px;
  gap: 56px;
}

.navbar__link {
  color: var(--color-nav-text);
  text-shadow: 0px 8px 16px 0px var(--color-nav-text-shadow);
  font-size: 16px;
  font-style: normal;
  font-weight: 500;
  line-height: 24px;
  text-decoration-line: underline;
}

@media screen and (max-width: 820px) {
  .navbar {
    display: none;
  }
}

</style>