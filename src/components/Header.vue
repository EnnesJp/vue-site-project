<template>
  <header>
    <div class="wrapper">
      <img src="@/assets/images/logo.png" alt="Logo">
      <div class="navbar">
        <RouterLink to="/products">Product</RouterLink>
        <RouterLink to="/blog">Blog</RouterLink>
        <RouterLink to="/support">Support</RouterLink>
        <RouterLink to="/login">Login</RouterLink>
        <div class="btn btn-primary">
          <RouterLink to="/register">Get Access</RouterLink>
        </div>
      </div>
    </div>
  </header>
</template>

<style scoped>

.wrapper {
  display: flex;
  position: absolute;
  top: 0;
  width: 100vw;
  padding: 40px 140px;
  align-items: center;
}
.wrapper .navbar {
  display: flex;
  justify-content: flex-end;
  align-items: center;
  width: 100%;
  padding-right: 20px;
  gap: 56px;
}

.wrapper .navbar a {
  color: var(--color-nav-text);
  text-shadow: 0px 8px 16px 0px var(--color-nav-text-shadow);
  font-size: 16px;
  font-style: normal;
  font-weight: 500;
  line-height: 24px;
  text-decoration-line: underline;
}

.wrapper .navbar .btn a {
  text-decoration: none;
}

</style>