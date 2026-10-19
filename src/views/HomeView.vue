<script setup>
import SidebarNavigation from '@/components/layout/SidebarNavigation.vue'
import HeroSection from '@/components/home/HeroSection.vue'
import InterestLinks from '@/components/home/InterestLinks.vue'
import SafetyCards from '@/components/home/SafetyCards.vue'
import { assetPath } from '@/utils/asset-path'
</script>

<template>
  <div class="page-layout">
    <div class="sidebar-column">
      <a class="institutional-logo" href="#inicio" aria-label="Gobierno de México y Comisión Federal de Electricidad">
        <img :src="assetPath('assets/logos/gobierno.png')" alt="Gobierno de México y CFE" />
      </a>
      <SidebarNavigation />
    </div>
    <div class="page-content">
      <HeroSection />
      <div class="content-grid">
        <InterestLinks />
        <SafetyCards />
      </div>
    </div>
  </div>
</template>

<style scoped>
.page-layout {
  display: grid;
  grid-template-columns: 300px minmax(0, 1fr);
  width: 100%;
  margin: 0 auto;
}

.sidebar-column {
  background: #fafafa;
}

.institutional-logo {
  display: block;
  padding: 1rem;
  background: var(--color-white);
}

.institutional-logo img {
  display: block;
  width: 100%;
  height: auto;
}

.page-content {
  min-width: 0;
}

.content-grid {
  display: grid;
  grid-template-columns: minmax(0, 1fr) minmax(270px, 0.8fr);
  gap: 2rem;
  padding: 2.25rem;
}

@media (max-width: 900px) {
  .page-layout {
    display: block;
  }

  .sidebar-column {
    display: none;
  }
}

@media (max-width: 650px) {
  .content-grid {
    display: block;
    padding: 1.25rem;
  }
}
</style>
