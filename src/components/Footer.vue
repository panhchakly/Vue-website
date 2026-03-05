<template>
  <footer class="footer">
    <div class="footer-container">
      <div class="footer-content">
        <div class="footer-column">
          <h3>BrandName</h3>
          <p>Building innovative solutions for a better tomorrow.</p>
        </div>

        <div class="footer-column">
          <h4>Company</h4>
          <ul>
            <li><a href="#about">About Us</a></li>
            <li><a href="#careers">Careers</a></li>
            <li><a href="#blog">Blog</a></li>
            <li><a href="#press">Press</a></li>
          </ul>
        </div>

        <div class="footer-column">
          <h4>Resources</h4>
          <ul>
            <li><a href="#docs">Documentation</a></li>
            <li><a href="#support">Support</a></li>
            <li><a href="#community">Community</a></li>
            <li><a href="#faq">FAQ</a></li>
          </ul>
        </div>

        <div class="footer-column">
          <h4>Legal</h4>
          <ul>
            <li><a href="#privacy">Privacy Policy</a></li>
            <li><a href="#terms">Terms of Service</a></li>
            <li><a href="#cookies">Cookie Policy</a></li>
          </ul>
        </div>
      </div>

      <div class="footer-bottom">
        <p>&copy; 2026 BrandName. All rights reserved.</p>
        <div class="social-links">
          <a href="#twitter" aria-label="Twitter">𝕏</a>
          <a href="#linkedin" aria-label="LinkedIn">in</a>
          <a href="#github" aria-label="GitHub">GH</a>
        </div>
      </div>
    </div>
  </footer>
</template>

<script setup lang="ts">
</script>

<style scoped>
.footer {
  background-color: #1a1a1a;
  color: #ffffff;
  padding: 4rem 2rem 2rem 2rem;
}

.footer-container {
  max-width: 1200px;
  margin: 0 auto;
}

.footer-content {
  display: grid;
  grid-template-columns: 2fr 1fr 1fr 1fr;
  gap: 3rem;
  margin-bottom: 3rem;
}

.footer-column h3 {
  font-size: 1.5rem;
  font-weight: 700;
  margin: 0 0 1rem 0;
}

.footer-column h4 {
  font-size: 1.1rem;
  font-weight: 600;
  margin: 0 0 1rem 0;
  color: #ffffff;
}

.footer-column p {
  color: #b0b0b0;
  line-height: 1.6;
  margin: 0;
}

.footer-column ul {
  list-style: none;
  padding: 0;
  margin: 0;
}

.footer-column ul li {
  margin-bottom: 0.75rem;
}

.footer-column ul li a {
  color: #b0b0b0;
  text-decoration: none;
  transition: color 0.3s ease;
}

.footer-column ul li a:hover {
  color: #ffffff;
}

.footer-bottom {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding-top: 2rem;
  border-top: 1px solid #333333;
}

.footer-bottom p {
  color: #b0b0b0;
  margin: 0;
}

.social-links {
  display: flex;
  gap: 1.5rem;
}

.social-links a {
  color: #b0b0b0;
  text-decoration: none;
  font-size: 1.2rem;
  transition: color 0.3s ease;
}

.social-links a:hover {
  color: #0066cc;
}

@media (max-width: 768px) {
  .footer {
    padding: 3rem 1.5rem 2rem 1.5rem;
  }

  .footer-content {
    grid-template-columns: 1fr;
    gap: 2rem;
  }

  .footer-bottom {
    flex-direction: column;
    gap: 1.5rem;
    text-align: center;
  }
}
</style>
