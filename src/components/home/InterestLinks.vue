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
