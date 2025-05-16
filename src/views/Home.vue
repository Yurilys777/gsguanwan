<template>
  <div class="relative min-h-screen bg-gray-900">
    <!-- 流星背景 -->
    <div class="fixed inset-0 z-0">
      <falling-stars-background
        color="255, 255, 255"
        :count="150"
        :speed="2"
        :trailLength="25"
      />
    </div>
    
    <!-- 页面内容 -->
    <div class="relative z-10">
      <hero-section />
      <features-section />
      <solutions-section />
      <testimonials-section />
      <portfolio-section />
    </div>
  </div>
</template>

<script setup>
import HeroSection from '../components/HeroSection.vue'
import FeaturesSection from '../components/FeaturesSection.vue'
import SolutionsSection from '../components/SolutionsSection.vue'
import TestimonialsSection from '../components/TestimonialsSection.vue'
import PortfolioSection from '../components/PortfolioSection.vue'
import FallingStarsBackground from '../components/FallingStarsBackground.vue'
</script>

<style>
/* 优化滚动行为 */
html {
  scroll-behavior: smooth;
}

/* 确保内容在背景之上 */
.relative {
  isolation: isolate;
}
</style>