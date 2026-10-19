<script setup>
import { assetPath } from '@/utils/asset-path'
</script>

<template>
  <section id="inicio" class="hero-section">
    <div class="hero-heading">
      <h1>Gerencia Regional de Transmisión Central</h1>
      <p>Zona de Operación de Transmisión Puebla Tlaxcala</p>
    </div>
    <div class="hero-image">
      <img :src="assetPath('assets/images/centro-control.png')" alt="Centro de control de transmisión" />
    </div>
    <p class="image-caption">
      Centro de control, Zona de Operación de Transmisión Puebla-Tlaxcala, 2026
    </p>
  </section>
</template>

<style scoped>
.hero-heading {
  padding: 1.5rem 1rem;
  background: var(--color-green);
  color: var(--color-white);
  text-align: center;
  text-transform: uppercase;
}

.hero-heading h1,
.hero-heading p {
  margin: 0;
}

.hero-heading h1 {
  color: #000;
  font-size: clamp(1.3rem, 3vw, 2.15rem);
}

.hero-heading p {
  margin-top: 0.3rem;
  font-size: clamp(1.15rem, 2.5vw, 1.85rem);
  font-weight: 700;
}

.hero-image {
  height: clamp(260px, 32vw, 420px);
  overflow: hidden;
}

.hero-image img {
  display: block;
  width: 100%;
  height: 100%;
  object-fit: cover;
  object-position: center;
}

.image-caption {
  margin: 0;
  padding: 0.8rem 1rem;
  background: var(--color-yellow);
  font-size: 1rem;
  text-align: center;
}

@media (max-width: 650px) {
  .hero-image {
    height: 240px;
  }
}
</style>
