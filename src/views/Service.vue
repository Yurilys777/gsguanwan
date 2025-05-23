<template>
  <div class="relative min-h-screen py-32 px-4 sm:px-6 lg:px-8">
    <!-- 背景特效 -->
    <div class="fixed inset-0 z-0">
      <falling-stars-background
        color="255, 255, 255"
        :count="120"
        :speed="1.8"
        :trailLength="22"
      />
    </div>
    
    <!-- 页面内容 -->
    <div class="relative z-10 max-w-7xl mx-auto">
      <div class="text-center mb-16">
        <h1 class="text-4xl sm:text-5xl font-bold mb-4">
          <span class="text-transparent bg-clip-text bg-gradient-to-r from-blue-500 to-purple-500">
            技术服务
          </span>
        </h1>
        <p class="text-lg text-white/60 max-w-2xl mx-auto">
          为企业提供全方位的智能办公解决方案
        </p>
      </div>

      <!-- 服务卡片网格 -->
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
        <!-- 智能办公系统 -->
        <div class="group bg-gray-800/50 backdrop-blur-xl rounded-2xl p-8 border border-gray-700/50 hover:bg-gray-800/70 transition-all duration-300 hover:-translate-y-1">
          <div class="w-12 h-12 bg-blue-500/20 rounded-lg flex items-center justify-center mb-4 group-hover:bg-blue-500/30 transition-colors">
            <svg class="w-6 h-6 text-blue-400" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9.75 17L9 20l-1 1h8l-1-1-.75-3M3 13h18M5 17h14a2 2 0 002-2V5a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z" />
            </svg>
          </div>
          <h3 class="text-xl font-semibold text-white mb-4">智能办公系统</h3>
          <p class="text-gray-300">提供一站式智能办公解决方案，包括文档管理、任务协作、工作流程等功能</p>
        </div>

        <!-- 数据分析 -->
        <div class="group bg-gray-800/50 backdrop-blur-xl rounded-2xl p-8 border border-gray-700/50 hover:bg-gray-800/70 transition-all duration-300 hover:-translate-y-1">
          <div class="w-12 h-12 bg-purple-500/20 rounded-lg flex items-center justify-center mb-4 group-hover:bg-purple-500/30 transition-colors">
            <svg class="w-6 h-6 text-purple-400" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M16 8v8m-4-5v5m-4-2v2m-2 4h12a2 2 0 002-2V6a2 2 0 00-2-2H6a2 2 0 00-2 2v12a2 2 0 002 2z" />
            </svg>
          </div>
          <h3 class="text-xl font-semibold text-white mb-4">数据分析</h3>
          <p class="text-gray-300">通过AI技术分析企业数据，提供决策支持和业务洞察</p>
        </div>

        <!-- 云服务 -->
        <div class="group bg-gray-800/50 backdrop-blur-xl rounded-2xl p-8 border border-gray-700/50 hover:bg-gray-800/70 transition-all duration-300 hover:-translate-y-1">
          <div class="w-12 h-12 bg-green-500/20 rounded-lg flex items-center justify-center mb-4 group-hover:bg-green-500/30 transition-colors">
            <svg class="w-6 h-6 text-green-400" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 15a4 4 0 004 4h9a5 5 0 10-.1-9.999 5.002 5.002 0 10-9.78 2.096A4.001 4.001 0 003 15z" />
            </svg>
          </div>
          <h3 class="text-xl font-semibold text-white mb-4">云服务</h3>
          <p class="text-gray-300">安全可靠的云存储和云计算服务，助力企业数字化转型</p>
        </div>

        <!-- 人工智能 -->
        <div class="group bg-gray-800/50 backdrop-blur-xl rounded-2xl p-8 border border-gray-700/50 hover:bg-gray-800/70 transition-all duration-300 hover:-translate-y-1">
          <div class="w-12 h-12 bg-pink-500/20 rounded-lg flex items-center justify-center mb-4 group-hover:bg-pink-500/30 transition-colors">
            <svg class="w-6 h-6 text-pink-400" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9.663 17h4.673M12 3v1m6.364 1.636l-.707.707M21 12h-1M4 12H3m3.343-5.657l-.707-.707m2.828 9.9a5 5 0 117.072 0l-.548.547A3.374 3.374 0 0014 18.469V19a2 2 0 11-4 0v-.531c0-.895-.356-1.754-.988-2.386l-.548-.547z" />
            </svg>
          </div>
          <h3 class="text-xl font-semibold text-white mb-4">人工智能</h3>
          <p class="text-gray-300">智能算法助力业务优化，包括智能客服、预测分析、自动化决策等</p>
        </div>

        <!-- 安全防护 -->
        <div class="group bg-gray-800/50 backdrop-blur-xl rounded-2xl p-8 border border-gray-700/50 hover:bg-gray-800/70 transition-all duration-300 hover:-translate-y-1">
          <div class="w-12 h-12 bg-red-500/20 rounded-lg flex items-center justify-center mb-4 group-hover:bg-red-500/30 transition-colors">
            <svg class="w-6 h-6 text-red-400" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m5.618-4.016A11.955 11.955 0 0112 2.944a11.955 11.955 0 01-8.618 3.04A12.02 12.02 0 003 9c0 5.591 3.824 10.29 9 11.622 5.176-1.332 9-6.03 9-11.622 0-1.042-.133-2.052-.382-3.016z" />
            </svg>
          </div>
          <h3 class="text-xl font-semibold text-white mb-4">安全防护</h3>
          <p class="text-gray-300">全方位的数据安全保护，包括访问控制、加密传输、安全审计等</p>
        </div>

        <!-- 技术支持 -->
        <div class="group bg-gray-800/50 backdrop-blur-xl rounded-2xl p-8 border border-gray-700/50 hover:bg-gray-800/70 transition-all duration-300 hover:-translate-y-1">
          <div class="w-12 h-12 bg-yellow-500/20 rounded-lg flex items-center justify-center mb-4 group-hover:bg-yellow-500/30 transition-colors">
            <svg class="w-6 h-6 text-yellow-400" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M18.364 5.636l-3.536 3.536m0 5.656l3.536 3.536M9.172 9.172L5.636 5.636m3.536 9.192l-3.536 3.536M21 12a9 9 0 11-18 0 9 9 0 0118 0zm-5 0a4 4 0 11-8 0 4 4 0 018 0z" />
            </svg>
          </div>
          <h3 class="text-xl font-semibold text-white mb-4">技术支持</h3>
          <p class="text-gray-300">7x24小时专业技术支持，确保系统稳定运行，快速响应客户需求</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import FallingStarsBackground from '../components/FallingStarsBackground.vue'
</script> 