<script setup lang="ts">
import Header from '@/components/Header.vue'
import Footer from '@/components/Footer.vue'
</script>

<template>
  <div class="min-h-screen flex flex-col relative">
    <!-- Sticky Header -->
    <!-- <Header /> -->

    <!-- Content Bereich -->
    <main class="flex-1 overflow-x-hidden">
      <slot />
    </main>

    <!-- Footer -->
    <Footer />
  </div>
</template>

<style scoped></style>
