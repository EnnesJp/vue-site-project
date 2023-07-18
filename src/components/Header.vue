<template>
  <div class="header">
    <div class="container">
      <img src="@/assets/images/logo.png" alt="Logo">
      <div class="navbar">
        <RouterLink class="navbar__link" to="/products">Product</RouterLink>
        <RouterLink class="navbar__link" to="/blog">Blog</RouterLink>
        <RouterLink class="navbar__link" to="/support">Support</RouterLink>
        <RouterLink class="navbar__link" to="/login">Login</RouterLink>
        <div class="btn btn-primary">
          <RouterLink to="/register">Get Access</RouterLink>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>

.header {
  position: absolute;
  top: 0;
  width: 100vw;
  padding: 40px 0;
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

</style>