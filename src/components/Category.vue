<template>
  <section class="category">
    <div class="category-container">
      <h2 class="section-title">Our Categories</h2>
      <p class="section-subtitle">Explore the different categories we offer</p>

      <div class="features-grid">
        <div v-for="feature in features" :key="feature.id" class="feature-card">
          <div class="feature-icon">{{ feature.icon }}</div>
          <h3 class="feature-title">{{ feature.title }}</h3>
          <p class="feature-description">{{ feature.description }}</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
import { ref } from 'vue';

interface Feature {
  id: number;
  icon: string;
  title: string;
  description: string;
}

const features = ref<Feature[]>([
  {
    id: 1,
    icon: '🍕',
    title: 'Pizzas',
    description: 'Delicious and customizable pizzas made with the freshest ingredients.'
  },
  {
    id: 2,
    icon: '🍔',
    title: 'Burgers',
    description: 'Juicy and flavorful burgers crafted with premium meats and creative toppings.'
  },
  {
    id: 3,
    icon: '🥖',
    title: 'Bread',
    description: 'Freshly baked bread with a variety of flavors and textures to satisfy every palate.'
  },
  {
    id: 4,
    icon: '🍰',
    title: 'Desserts',
    description: 'Indulgent and delightful desserts that are the perfect way to end your meal on a sweet note.'
  }
]);
</script>

<style scoped>
.category {
  padding: 6rem 2rem;
  background-color: #f8f9fa;
}

.category-container {
  max-width: 1200px;
  margin: 0 auto;
}

.section-title {
  text-align: center;
  font-size: 2.5rem;
  font-weight: 700;
  color: #1a1a1a;
  margin: 0 0 1rem 0;
  font-family: "Fugaz One", sans-serif;
  font-style: normal;
}

.section-subtitle {
  text-align: center;
  font-size: 1.1rem;
  color: #6b6b6b;
  margin: 0 0 4rem 0;
}

.features-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 2rem;
}

.feature-card {
  background-color: white;
  padding: 2.5rem 2rem;
  border-radius: 12px;
  text-align: center;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.05);
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.feature-card:hover {
  transform: translateY(-8px);
  box-shadow: 0 12px 24px rgba(0, 0, 0, 0.1);
}

.feature-icon {
  font-size: 3rem;
  margin-bottom: 1.5rem;
}

.feature-title {
  font-size: 1.4rem;
  font-weight: 600;
  color: #1a1a1a;
  margin: 0 0 1rem 0;
}

.feature-description {
  font-size: 1rem;
  line-height: 1.6;
  color: #6b6b6b;
  margin: 0;
}

@media (max-width: 768px) {
  .category {
    padding: 4rem 1.5rem;
  }

  .section-title {
    font-size: 2rem;
  }

  .features-grid {
    grid-template-columns: 1fr;
    gap: 1.5rem;
  }
}
</style>
