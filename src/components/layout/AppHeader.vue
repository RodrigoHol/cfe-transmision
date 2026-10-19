<script setup>
import { navigationItems } from '@/data/navigation'
</script>

<template>
  <header class="site-header">
    <nav class="top-navigation" aria-label="Navegación principal">
      <a
        v-for="item in navigationItems"
        :key="item.label"
        class="navigation-link"
        :href="item.href"
      >
        {{ item.label }}
      </a>
      <a class="login-button" href="#iniciar-sesion">Iniciar sesión</a>
    </nav>
  </header>
</template>
