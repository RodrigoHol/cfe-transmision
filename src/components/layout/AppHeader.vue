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

<style scoped>
.site-header {
  position: sticky;
  top: 0;
  z-index: 10;
  box-shadow: var(--shadow-soft);
}

.top-navigation {
  display: flex;
  align-items: center;
  gap: clamp(1rem, 4vw, 3.5rem);
  min-height: 76px;
  padding: 0 clamp(1rem, 3vw, 3rem);
  background: var(--color-yellow);
}

.navigation-link {
  text-decoration: none;
  white-space: nowrap;
}

.navigation-link:hover {
  text-decoration: underline;
}

.login-button {
  margin-left: auto;
  border: 1px solid var(--color-text);
  background: var(--color-white);
  padding: 0.6rem 1.6rem;
  text-decoration: none;
}

@media (max-width: 900px) {
  .top-navigation {
    flex-wrap: wrap;
    gap: 0.8rem 1.2rem;
    padding-block: 0.8rem;
  }

  .login-button {
    margin-left: 0;
  }
}
</style>
