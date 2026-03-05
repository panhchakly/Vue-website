<template>
  <section class="banner">
    <div class="banner-background">
      <img
        src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQiqraeibjhNbzaL2PQLlvTjGGU25uQzBsc5w&s?auto=compress&cs=tinysrgb&w=1600"
        alt="Business team collaboration"
        class="banner-image"
      />
      <div class="banner-overlay"></div>
    </div>
    <div class="banner-content">
      <h1 class="banner-title">Welcome to Our Platform</h1>
      <p class="banner-description">
        Transform your business with innovative solutions designed for the modern world
      </p>
      <div class="banner-actions">
        <button class="primary-btn">Learn More</button>
        <button class="secondary-btn">Watch Demo</button>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
</script>

<style scoped>
.banner {
  position: relative;
  color: white;
  padding: 8rem 2rem;
  text-align: center;
  min-height: 600px;
  display: flex;
  align-items: center;
  justify-content: center;
  overflow: hidden;
}

.banner-background {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  z-index: 1;
}

.banner-image {
  width: 100%;
  height: 100%;
  object-fit: cover;
  display: block;
}

.banner-overlay {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: linear-gradient(135deg, rgba(0, 102, 204, 0.7) 0%, rgba(0, 82, 163, 0.7) 100%);
  z-index: 2;
}

.banner-content {
  position: relative;
  z-index: 3;
  max-width: 800px;
  margin: 0 auto;
}

.banner-title {
  font-size: 3.5rem;
  font-weight: 700;
  margin: 0 0 1.5rem 0;
  line-height: 1.2;
  animation: fadeInUp 0.8s ease;
  text-shadow: 2px 2px 8px rgba(0, 0, 0, 0.3);
  font-family: "Black Ops One", system-ui;
  font-style: normal;

}

.banner-description {
  font-size: 1.25rem;
  line-height: 1.8;
  margin: 0 0 2.5rem 0;
  opacity: 0.95;
  animation: fadeInUp 0.8s ease 0.2s backwards;
  text-shadow: 1px 1px 4px rgba(0, 0, 0, 0.3);
}

.banner-actions {
  display: flex;
  gap: 1rem;
  justify-content: center;
  animation: fadeInUp 0.8s ease 0.4s backwards;
}

.primary-btn,
.secondary-btn {
  padding: 1rem 2rem;
  font-size: 1rem;
  font-weight: 600;
  border-radius: 6px;
  cursor: pointer;
  transition: all 0.3s ease;
  border: 2px solid white;
}

.primary-btn {
  background-color: white;
  color: #0066cc;
}

.primary-btn:hover {
  background-color: transparent;
  color: white;
  transform: translateY(-2px);
  box-shadow: 0 8px 16px rgba(0, 0, 0, 0.2);
}

.secondary-btn {
  background-color: transparent;
  color: white;
}

.secondary-btn:hover {
  background-color: white;
  color: #0066cc;
  transform: translateY(-2px);
  box-shadow: 0 8px 16px rgba(0, 0, 0, 0.2);
}

@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translateY(30px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

@media (max-width: 768px) {
  .banner {
    padding: 5rem 1.5rem;
    min-height: 400px;
  }

  .banner-title {
    font-size: 2.5rem;
  }

  .banner-description {
    font-size: 1.1rem;
  }

  .banner-actions {
    flex-direction: column;
    align-items: center;
  }

  .primary-btn,
  .secondary-btn {
    width: 100%;
    max-width: 300px;
  }
}
</style>
