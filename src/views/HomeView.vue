<script setup>
import SidebarNavigation from '@/components/layout/SidebarNavigation.vue'
import HeroSection from '@/components/home/HeroSection.vue'
import InterestLinks from '@/components/home/InterestLinks.vue'
import SafetyCards from '@/components/home/SafetyCards.vue'
</script>

<template>
  <div class="page-layout">
    <div class="sidebar-column">
      <a class="institutional-logo" href="#inicio" aria-label="Gobierno de México y Comisión Federal de Electricidad">
        <img src="/assets/logos/gobierno.png" alt="Gobierno de México y CFE" />
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
