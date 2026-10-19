<script setup>
import { sidebarItems } from '@/data/navigation'
</script>

<template>
  <aside class="sidebar" aria-label="Información del centro de trabajo">
    <ul>
      <li v-for="item in sidebarItems" :key="item">
        <a href="#">{{ item }}</a>
      </li>
    </ul>
  </aside>
</template>
