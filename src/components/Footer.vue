<script setup>
const footerLinks = [
  { id: 1, text: 'Home', url: '#' },
  { id: 2, text: 'Types of Plants', url: '#' },
  { id: 3, text: 'Contact Us', url: '#' },
  { id: 4, text: 'Privacy Policy', url: '#' }
]
const socialLinks = [
  { id: 1, name: 'FB', url: '#', label: 'Facebook' },
  { id: 2, name: 'TW', url: '#', label: 'Twitter' },
  { id: 3, name: 'LI', url: '#', label: 'LinkedIn' }
]
</script>

<template>
  <footer class="site-footer">
    <div class="footer-column footer-about">
      <div class="footer-logo">
        <img src="/logo-icon.png" alt="Planto Logo" class="logo-img">
        <span class="logo-text">Planto.</span>
      </div>
      <p class="footer-description">
        We help you find the perfect green companions to bring freshness, style, and cleaner air straight into your
        modern home.
      </p>
      <ul class="social-list">
        <li v-for="social in socialLinks" :key="social.id">
          <a :href="social.url" :aria-label="social.label" class="social-link">{{ social.name }}</a>
        </li>
      </ul>
    </div>

    <div class="footer-column footer-navigation">
      <h3 class="footer-title">Quick Links</h3>
      <ul class="footer-nav-list">
        <li v-for="link in footerLinks" :key="link.id">
          <a :href="link.url" class="footer-nav-link">{{ link.text }}</a>
        </li>
      </ul>
    </div>

    <div class="footer-column footer-subscribe">
      <h3 class="footer-title">For Every Update</h3>

      <form class="subscribe-form" @submit.prevent>
        <input type="email" placeholder="Enter Email" class="subscribe-input" required>
        <button type="submit" class="btn-subscribe">Subscribe</button>
      </form>

      <p class="copyright">Planto © All rights reserved</p>
    </div>
  </footer>
</template>

<style scoped>
.site-footer {
  padding: 80px 60px 40px;
  display: flex;
  justify-content: space-between;
  gap: 40px;
  background-color: #222C1D;
  color: #FFFFFF;
}

.footer-column {
  display: flex;
  flex-direction: column;
}

.footer-title {
  font-size: 28px;
  font-weight: 600;
  margin: 0 0 45px 0;
}

.footer-about {
  width: 500px;
}

.footer-logo {
  display: flex;
  align-items: center;
  gap: 15px;
  color: rgba(255, 255, 255, 0.75);
}

.logo-img {
  width: 65px;
  height: 65px;
}

.logo-text {
  font-size: 40px;
  font-weight: bold;
}

.footer-description {
  margin-top: 30px;
  font-size: 24px;
  line-height: 1.5;
  color: rgba(255, 255, 255, 0.8px);
}

.social-list {
  margin-top: 60px;
  padding: 0;
  list-style: none;
  display: flex;
  gap: 35px;
}

.social-link {
  font-size: 24px;
  font-weight: bold;
  color: #FFFFFF;
  text-decoration: none;
  opacity: 0.7;
  transition: opacity 0.3s ease;
}

.social-link:hover {
  opacity: 1;
}

.footer-navigation {
  width: 220px;
}

.footer-nav-list {
  padding: 0;
  margin: 0;
  list-style: none;
  display: flex;
  flex-direction: column;
  gap: 25px;
}

.footer-nav-link {
  font-size: 24px;
  color: #FFFFFF;
  text-decoration: none;
  opacity: 0.8;
  transition: opacity 0.3s ease, padding-left 0.3s ease;
}

.footer-nav-link:hover {
  opacity: 1;
  padding-left: 5px;
}

.footer-subscribe {
  width: 525px;
}


.subscribe-form {
  display: flex;
  align-items: center;
  padding: 4px;
  width: 100%;
  height: 70px;
  border: 2px solid #FFFFFF;
  border-radius: 12px;
  background: transparent;
}

.subscribe-input {
  flex: 1;
  height: 100%;
  padding: 0 20px;
  font-size: 22px;
  background: none;
  border: none;
  color: #FFFFFF;
  outline: none;
}

.subscribe-input::placeholder {
  color: rgba(255, 255, 255, 0.5);
}

.btn-subscribe {
  height: 100%;
  padding: 0 35px;
  font-size: 20px;
  font-weight: bold;
  color: #000000;
  background-color: #FFFFFF;
  border: none;
  border-radius: 8px;
  cursor: pointer;
  transition: background-color 0.3s ease, transform 0.2s ease;
}

.btn-subscribe:hover {
  background-color: #e2e2e2;
}

.btn-subscribe:active {
  transform: scale(0.98);
}

.copyright {
  margin-top: auto;
  font-size: 22px;
  color: rgba(255, 255, 255, 0.6);
}
</style>