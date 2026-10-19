<script setup>
import { sidebarItems } from '@/data/navigation'
</script>

<template>
  <aside class="sidebar" aria-label="Información del centro de trabajo">
    <ul>
      <li
        v-for="item in sidebarItems"
        :key="item.label"
        class="sidebar-item"
        :class="`sidebar-item--level-${item.level}`"
      >
        <a href="#">{{ item.label }}</a>
      </li>
    </ul>
  </aside>
</template>

<style scoped>
.sidebar {
  padding: 1.25rem 1.5rem;
}

.sidebar ul {
  display: grid;
  gap: 0.55rem;
  margin: 0;
  padding: 0;
  list-style: none;
}

.sidebar-item--level-1 {
  padding-left: 1rem;
}

.sidebar-item--level-2 {
  padding-left: 2rem;
}

.sidebar a {
  display: block;
  color: var(--color-muted);
  font-size: 0.95rem;
  font-weight: 600;
  text-decoration: none;
}

.sidebar a:hover {
  text-decoration: underline;
}

.sidebar a::before {
  content: '› ';
  color: var(--color-gold);
}
</style>
