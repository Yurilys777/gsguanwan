<template>
  <div class="min-h-screen flex flex-col">
    <nav-bar />
    <main class="flex-grow">
      <router-view />
    </main>
    <app-footer />
  </div>
</template>

<script setup>
import NavBar from './components/NavBar.vue'
import AppFooter from './components/Footer.vue'
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap');

:root {
  color-scheme: light dark;
}

body {
  font-family: 'Inter', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.3s ease;
}

.fade-enter-from,
.fade-leave-to {
  opacity: 0;
}

/* 主题切换过渡 */
.theme-transition {
  transition: background-color 0.3s ease,
              color 0.3s ease,
              border-color 0.3s ease,
              box-shadow 0.3s ease;
}

/* 渐变文本通用类 */
.gradient-text {
  @apply bg-gradient-to-r from-primary-500 to-secondary-500 bg-clip-text text-transparent;
}

/* 渐变按钮通用类 */
.gradient-button {
  @apply bg-gradient-to-r from-primary-500 to-secondary-500 
         hover:from-primary-600 hover:to-secondary-600 
         text-white transition-all duration-200;
}
</style> 