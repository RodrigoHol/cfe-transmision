<script setup>
import { safetyCards } from '@/data/safety-cards'
</script>

<template>
  <section class="safety-section" aria-labelledby="safety-title">
    <h2 id="safety-title">Información de seguridad</h2>
    <div class="safety-list">
      <article v-for="card in safetyCards" :key="card.title" class="safety-card">
        <img class="safety-image" :src="card.image" :alt="card.alt" />
        <h3>{{ card.title }}</h3>
      </article>
    </div>
  </section>
</template>

<style scoped>
.safety-section h2 {
  width: fit-content;
  margin: 0 auto 1.25rem;
  padding: 0.55rem 2.5rem;
  background: var(--color-yellow);
  font-size: 1.2rem;
  font-weight: 400;
}

.safety-list {
  display: grid;
  gap: 1.5rem;
}

.safety-card {
  width: 100%;
}

.safety-image {
  display: block;
  width: 100%;
  height: auto;
  margin: 0 auto;
  object-fit: contain;
}

.safety-card h3 {
  margin: 0;
  padding: 0.6rem;
  font-size: 0.85rem;
  text-align: center;
}
</style>
