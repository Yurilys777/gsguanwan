<template>
  <div class="relative min-h-screen py-32 px-4 sm:px-6 lg:px-8">
    <!-- 背景特效 -->
    <div class="fixed inset-0 z-0">
      <falling-stars-background
        color="255, 255, 255"
        :count="100"
        :speed="1.5"
        :trailLength="20"
      />
    </div>
    
    <!-- 页面内容 -->
    <div class="relative z-10 max-w-7xl mx-auto">
      <div class="text-center mb-16">
        <h1 class="text-4xl sm:text-5xl font-bold mb-4">
          <span class="text-transparent bg-clip-text bg-gradient-to-r from-blue-500 to-purple-500">
            关于我们
          </span>
        </h1>
        <p class="text-lg text-white/60 max-w-2xl mx-auto">
          专注于为企业提供智能化办公解决方案
        </p>
      </div>

      <!-- 公司简介卡片 -->
      <div class="bg-gray-800/50 backdrop-blur-xl rounded-2xl p-8 mb-12 border border-gray-700/50">
        <h2 class="text-2xl font-semibold text-white mb-6">公司简介</h2>
        <p class="text-gray-300 leading-relaxed">
          我们是一家致力于为企业提供智能化办公解决方案的科技公司。通过持续创新和技术积累，
          我们帮助企业实现数字化转型，提升运营效率。
        </p>
      </div>

      <!-- 数据统计卡片 -->
      <div class="grid grid-cols-1 md:grid-cols-2 gap-8 mb-12">
        <div class="bg-gray-800/50 backdrop-blur-xl rounded-2xl p-8 border border-gray-700/50">
          <div class="text-4xl font-bold text-blue-400 mb-2">1000+</div>
          <div class="text-xl text-gray-300">服务企业</div>
        </div>
        <div class="bg-gray-800/50 backdrop-blur-xl rounded-2xl p-8 border border-gray-700/50">
          <div class="text-4xl font-bold text-purple-400 mb-2">99%</div>
          <div class="text-xl text-gray-300">客户满意度</div>
        </div>
      </div>

      <!-- 特色优势卡片 -->
      <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
        <div class="bg-gray-800/50 backdrop-blur-xl rounded-2xl p-8 border border-gray-700/50">
          <div class="w-12 h-12 bg-blue-500/20 rounded-lg flex items-center justify-center mb-4">
            <svg class="w-6 h-6 text-blue-400" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 20h5v-2a3 3 0 00-5.356-1.857M17 20H7m10 0v-2c0-.656-.126-1.283-.356-1.857M7 20H2v-2a3 3 0 015.356-1.857M7 20v-2c0-.656.126-1.283.356-1.857m0 0a5.002 5.002 0 019.288 0M15 7a3 3 0 11-6 0 3 3 0 016 0zm6 3a2 2 0 11-4 0 2 2 0 014 0zM7 10a2 2 0 11-4 0 2 2 0 014 0z" />
            </svg>
          </div>
          <h3 class="text-xl font-semibold text-white mb-4">拥有多年经验的研发团队</h3>
          <p class="text-gray-300">持续创新，为客户提供最优解决方案</p>
        </div>
        <div class="bg-gray-800/50 backdrop-blur-xl rounded-2xl p-8 border border-gray-700/50">
          <div class="w-12 h-12 bg-purple-500/20 rounded-lg flex items-center justify-center mb-4">
            <svg class="w-6 h-6 text-purple-400" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m5.618-4.016A11.955 11.955 0 0112 2.944a11.955 11.955 0 01-8.618 3.04A12.02 12.02 0 003 9c0 5.591 3.824 10.29 9 11.622 5.176-1.332 9-6.03 9-11.622 0-1.042-.133-2.052-.382-3.016z" />
            </svg>
          </div>
          <h3 class="text-xl font-semibold text-white mb-4">服务过众多行业客户</h3>
          <p class="text-gray-300">深入理解不同行业的业务需求</p>
        </div>
        <div class="bg-gray-800/50 backdrop-blur-xl rounded-2xl p-8 border border-gray-700/50">
          <div class="w-12 h-12 bg-blue-500/20 rounded-lg flex items-center justify-center mb-4">
            <svg class="w-6 h-6 text-blue-400" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M21 12a9 9 0 01-9 9m9-9a9 9 0 00-9-9m9 9H3m9 9a9 9 0 01-9-9m9 9c1.657 0 3-4.03 3-9s-1.343-9-3-9m0 18c-1.657 0-3-4.03-3-9s1.343-9 3-9m-9 9a9 9 0 019-9" />
            </svg>
          </div>
          <h3 class="text-xl font-semibold text-white mb-4">全方位技术支持</h3>
          <p class="text-gray-300">提供全方位的技术支持和售后服务</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import FallingStarsBackground from '../components/FallingStarsBackground.vue'
</script> 