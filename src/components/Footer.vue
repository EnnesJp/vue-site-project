<template>
  <div class="footer">
    <div class="container">
      <div class="footer-logo">
        <img src="@/assets/images/logo.png" alt="Logo">
        <p>{{ $t('footer.description') }}</p>
      </div>
      <div class="footer-links">
        <div class="footer-links-column">
          <h4 class="footer-links-column-title">{{ $t('footer.company') }}</h4>
          <a href="#" class="footer-links-column-link">{{ $t('footer.product') }}</a>
          <a href="#" class="footer-links-column-link">{{ $t('footer.blog') }}</a>
          <a href="#" class="footer-links-column-link">{{ $t('footer.support') }}</a>
        </div>
        <div class="footer-links-column">
          <h4 class="footer-links-column-title">{{ $t('footer.features') }}</h4>
          <a href="#" class="footer-links-column-link">{{ $t('footer.screenSharing') }}</a>
          <a href="#" class="footer-links-column-link">{{ $t('footer.apps') }}</a>
          <a href="#" class="footer-links-column-link">{{ $t('footer.fileSharing') }}</a>
          <a href="#" class="footer-links-column-link">{{ $t('footer.userManagement') }}</a>
        </div>
        <div class="footer-links-column">
          <h4 class="footer-links-column-title">{{ $t('footer.contact') }}</h4>
          <a href="#" class="footer-links-column-link">{{ $t('footer.email') }}</a>
          <a href="#" class="footer-links-column-link">{{ $t('footer.cell') }}</a>
          <a href="#" class="footer-links-column-link">{{ $t('footer.address') }}</a>
        </div>
      </div>
      <div class="footer-social">
        <a href="#"><img src="@/assets/images/icon-facebook.svg" alt="Facebook"></a>
        <a href="#"><img src="@/assets/images/icon-twitter.svg" alt="Twitter"></a>
        <a href="#"><img src="@/assets/images/icon-instagram.svg" alt="Instagram"></a>
      </div>
    </div>
  </div>
</template>

<style scoped>

.footer {
  position: relative;
  height: 500px;
  background: var(--color-background-footer);
  padding-top: 73px;
}

.footer .container {
  align-items: flex-start;
  gap: 130px;
}

.footer .footer-logo p{
  color: var(--color-text-white);
  font-size: 14px;
  font-style: normal;
  font-weight: 400;
  line-height: 23px;
  letter-spacing: 0.14px;
  max-width: 168px;
}

.footer .footer-links {
  display: flex;
  padding-top: 22px;
  gap: 85px;
}

.footer .footer-links .footer-links-column {
  display: flex;
  flex-direction: column;
}

.footer .footer-links .footer-links-column .footer-links-column-title {
  color: var(--color-heading-footer);
  font-size: 24px;
  font-style: normal;
  font-weight: 400;
  line-height: 30px; 
  margin-bottom: 16px;
}

.footer .footer-links .footer-links-column .footer-links-column-link {
  color: var(--color-text-white);
  font-size: 14px;
  font-style: normal;
  font-weight: 400;
  line-height: 23px;
  letter-spacing: 0.14px;
  text-decoration: none;
  margin-bottom: 12px;
}

.footer .footer-social {
  display: flex;
  gap: 12px;
}

</style>