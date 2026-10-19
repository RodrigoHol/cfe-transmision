<script setup>
import { interestLinks } from '@/data/interest-links'
</script>

<template>
  <section id="enlaces" class="interest-section" aria-labelledby="interest-title">
    <h2 id="interest-title">Sitios de interés</h2>
    <div class="interest-grid">
      <a v-for="item in interestLinks" :key="item.label" class="interest-link" :href="item.href">
        <img class="interest-logo" :src="item.logo" :alt="`Logo de ${item.label}`" />
        <span>{{ item.label }}</span>
      </a>
    </div>
  </section>
</template>

<style scoped>
.interest-section h2 {
  width: fit-content;
  margin: 0 auto 1.25rem;
  padding: 0.55rem 2.5rem;
  background: var(--color-yellow);
  font-size: 1.2rem;
  font-weight: 400;
}

.interest-grid {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 1.2rem 0.75rem;
}

.interest-link {
  display: grid;
  justify-items: center;
  gap: 0.35rem;
  color: var(--color-text);
  font-size: 0.8rem;
  text-align: center;
  text-decoration: none;
}

.interest-link:hover {
  text-decoration: underline;
}

.interest-logo {
  display: block;
  width: 58px;
  height: 58px;
  object-fit: contain;
}

@media (max-width: 650px) {
  .interest-grid {
    grid-template-columns: repeat(3, 1fr);
  }
}
</style>
