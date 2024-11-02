<script setup lang="ts">
import HeaderPage from './components/HeaderPage.vue'
import FooterPage from './components/FooterPage.vue'
import MainLayout from './components/layouts/MainLayout.vue'
</script>

<template>
  <MainLayout>
    <HeaderPage />
    <RouterView />
    <FooterPage />
  </MainLayout>
</template>
