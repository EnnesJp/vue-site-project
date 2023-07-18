<template>
  <div class="footer">
    <div class="container">
      <div class="footer-logo">
        <img src="@/assets/images/logo.png" alt="Logo">
        <p>Collaboration platform for mordern team </p>
      </div>
      <div class="footer-links">
        <div class="footer-links-column">
          <h4 class="footer-links-column-title">Company</h4>
          <a href="#" class="footer-links-column-link">Product</a>
          <a href="#" class="footer-links-column-link">Blog</a>
          <a href="#" class="footer-links-column-link">Support</a>
        </div>
        <div class="footer-links-column">
          <h4 class="footer-links-column-title">Features</h4>
          <a href="#" class="footer-links-column-link">Screen Sharing</a>
          <a href="#" class="footer-links-column-link">iOS & Android Apps</a>
          <a href="#" class="footer-links-column-link">File Sharing</a>
          <a href="#" class="footer-links-column-link">User Managment</a>
        </div>
        <div class="footer-links-column">
          <h4 class="footer-links-column-title">Contact Us</h4>
          <a href="#" class="footer-links-column-link">info@teamapp.com</a>
          <a href="#" class="footer-links-column-link">1-800-200-300</a>
          <a href="#" class="footer-links-column-link">1010 Sunset Blv. Palo Alto, California</a>
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