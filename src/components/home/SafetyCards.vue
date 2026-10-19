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
