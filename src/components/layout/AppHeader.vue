<script setup>
import { navigationItems } from '@/data/navigation'
</script>

<template>
  <header class="site-header">
    <nav class="top-navigation" aria-label="Navegación principal">
      <div class="navigation-links">
        <a
          v-for="item in navigationItems"
          :key="item.label"
          class="navigation-link"
          :href="item.href"
        >
          {{ item.label }}
        </a>
      </div>
      <a class="login-button" href="#iniciar-sesion">
        <span>Iniciar sesión</span>
      </a>
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
  justify-content: space-between;
  gap: 2rem;
  min-height: 78px;
  padding: 0 clamp(1rem, 4vw, 4rem);
  background: var(--color-yellow);
}

.navigation-links {
  display: flex;
  align-items: stretch;
  justify-content: space-between;
  flex: 1;
  max-width: 820px;
}

.navigation-link {
  position: relative;
  display: grid;
  align-items: center;
  padding: 0.5rem 0.75rem;
  color: var(--color-text);
  text-decoration: none;
  white-space: nowrap;
  transition:
    color 180ms ease,
    transform 180ms ease;
}

.navigation-link:hover,
.navigation-link:focus-visible {
  color: var(--color-green-dark);
  transform: translateY(-2px);
}

.navigation-link:focus-visible,
.login-button:focus-visible {
  outline: 3px solid rgb(8 123 53 / 35%);
  outline-offset: 3px;
}

.login-button {
  display: inline-flex;
  align-items: center;
  gap: 0.7rem;
  flex-shrink: 0;
  border: 1px solid var(--color-green-dark);
  border-radius: 999px;
  background: var(--color-green-dark);
  box-shadow: 0 5px 12px rgb(8 123 53 / 22%);
  color: var(--color-white);
  padding: 0.7rem 1.15rem 0.7rem 1.35rem;
  font-size: 0.95rem;
  font-weight: 700;
  text-decoration: none;
  transition:
    background-color 180ms ease,
    box-shadow 180ms ease,
    transform 180ms ease;
}

.login-button:hover {
  background: #05652b;
  box-shadow: 0 8px 18px rgb(8 123 53 / 30%);
  transform: translateY(-2px);
}

.login-button:hover {
  transform: translateX(3px);
}

@media (max-width: 900px) {
  .top-navigation {
    flex-wrap: wrap;
    gap: 0.5rem 1rem;
    padding-block: 0.8rem;
  }

  .navigation-links {
    flex-wrap: wrap;
    gap: 0.25rem 0.5rem;
    max-width: none;
  }

  .navigation-link {
    padding-inline: 0.5rem;
  }
}

@media (max-width: 650px) {
  .top-navigation {
    align-items: stretch;
  }

  .navigation-links {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    width: 100%;
  }

  .navigation-link {
    min-height: 2.5rem;
  }

  .login-button {
    justify-content: center;
    width: 100%;
  }
}
</style>
