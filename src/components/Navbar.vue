<template>
  <nav class="navbar">
    <div class="nav-container">
      <div class="logo">
        <h2>BrandName</h2>
      </div>
      <ul class="nav-links">
        <li><a href="#home">Home</a></li>
        <li><a href="#about">About</a></li>
        <li><a href="#services">Services</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
      <button class="cta-button">Get Started</button>
    </div>
  </nav>
</template>

<script setup lang="ts">
</script>

<style scoped>
.navbar {
  background-color: #ffffff;
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.05);
  position: sticky;
  top: 0;
  z-index: 100;
  padding: 1rem 0;
}

.nav-container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 2rem;
  display: flex;
  justify-content: space-between;
  align-items: center;
  font-family: "Black Ops One", system-ui;
  font-style: normal;
}

.logo h2 {
  margin: 0;
  font-size: 1.5rem;
  font-weight: 700;
  color: #1a1a1a;
}

.nav-links {
  display: flex;
  list-style: none;
  gap: 2rem;
  margin: 0;
  padding: 0;
}

.nav-links a {
  text-decoration: none;
  color: #4a4a4a;
  font-weight: 500;
  transition: color 0.3s ease;
}

.nav-links a:hover {
  color: #0066cc;
}

.cta-button {
  background-color: #0066cc;
  color: white;
  border: none;
  padding: 0.75rem 1.5rem;
  border-radius: 6px;
  font-weight: 600;
  cursor: pointer;
  transition: background-color 0.3s ease, transform 0.2s ease;
}

.cta-button:hover {
  background-color: #0052a3;
  transform: translateY(-2px);
}

@media (max-width: 768px) {
  .nav-links {
    display: none;
  }

  .nav-container {
    padding: 0 1rem;
  }
}
</style>
