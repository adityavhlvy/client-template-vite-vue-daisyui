<script setup>
import { RouterView } from 'vue-router'

import AppHeader from './components/AppHeader.vue'
</script>

<template>
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />

  <div class="h-screen flex flex-col">
    <header>
      <AppHeader />
    </header>

    <main class="h-full">
      <RouterView />
    </main>
  </div>
</template>
