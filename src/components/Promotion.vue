<template>
  <section class="category">
    <div class="category-container">
      <div class="features-grid">
        <div v-for="feature in features" :key="feature.id" class="feature-card">
          <img :src="feature.image_url" :alt="feature.title" class="feature-image">
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
import { ref } from 'vue';

interface Feature {
  id: number;
  title: string;
  image_url: string;
}

const features = ref<Feature[]>([
  {
    id: 1,
    title: 'Pizzas',
    image_url: 'https://source.unsplash.com/400x300/?pizza'
  },
  {
    id: 2,
    title: 'Burgers',
    image_url: 'https://source.unsplash.com/400x300/?burger'
  },
  {
    id: 3,
    title: 'Bread',
    image_url: 'https://source.unsplash.com/400x300/?bread'
  },
  {
    id: 4,
    title: 'Desserts',
    image_url: 'https://source.unsplash.com/400x300/?dessert'
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

.features-grid {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
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

@media (max-width: 768px) {
  .category {
    padding: 4rem 1.5rem;
  }
  .features-grid {
    grid-template-columns: 1fr;
    gap: 1.5rem;
  }
}
</style>
