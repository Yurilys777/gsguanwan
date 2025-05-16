<template>
  <section class="relative py-24 overflow-hidden">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="text-center mb-16">
        <h2 class="text-4xl sm:text-5xl font-bold mb-4">
          <span class="text-transparent bg-clip-text bg-gradient-to-r from-blue-500 to-purple-500">
            产品特性
          </span>
        </h2>
        <p class="text-xl text-gray-300">全方位的智能办公解决方案，助力企业效率提升</p>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
        <!-- 智能任务管理 -->
        <div class="group relative p-8 bg-gray-800/90 backdrop-blur-sm rounded-2xl border border-gray-700 hover:border-blue-500 transition-all duration-300 hover:-translate-y-2">
          <div class="absolute inset-0 bg-gradient-to-br from-blue-500/30 to-purple-500/30 rounded-2xl opacity-0 group-hover:opacity-100 transition-opacity duration-300"></div>
          <div class="relative">
            <div class="w-16 h-16 mb-6 bg-blue-500/30 rounded-2xl flex items-center justify-center">
              <svg class="w-8 h-8 text-blue-400" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-6 9l2 2 4-4"></path>
              </svg>
            </div>
            <h3 class="text-2xl font-bold text-white mb-4">智能任务管理</h3>
            <p class="text-gray-200 leading-relaxed">自动分配任务，智能跟踪进度，提高团队协作效率。采用AI算法优化任务分配，确保资源最优配置。</p>
          </div>
        </div>

        <!-- 自动化流程 -->
        <div class="group relative p-8 bg-gray-800/90 backdrop-blur-sm rounded-2xl border border-gray-700 hover:border-purple-500 transition-all duration-300 hover:-translate-y-2">
          <div class="absolute inset-0 bg-gradient-to-br from-purple-500/30 to-pink-500/30 rounded-2xl opacity-0 group-hover:opacity-100 transition-opacity duration-300"></div>
          <div class="relative">
            <div class="w-16 h-16 mb-6 bg-purple-500/30 rounded-2xl flex items-center justify-center">
              <svg class="w-8 h-8 text-purple-400" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 10V3L4 14h7v7l9-11h-7z"></path>
              </svg>
            </div>
            <h3 class="text-2xl font-bold text-white mb-4">自动化流程</h3>
            <p class="text-gray-200 leading-relaxed">智能工作流程自动化，减少人工操作，提高工作效率。支持自定义流程模板，灵活适应不同场景。</p>
          </div>
        </div>

        <!-- 数据分析 -->
        <div class="group relative p-8 bg-gray-800/90 backdrop-blur-sm rounded-2xl border border-gray-700 hover:border-green-500 transition-all duration-300 hover:-translate-y-2">
          <div class="absolute inset-0 bg-gradient-to-br from-green-500/30 to-teal-500/30 rounded-2xl opacity-0 group-hover:opacity-100 transition-opacity duration-300"></div>
          <div class="relative">
            <div class="w-16 h-16 mb-6 bg-green-500/30 rounded-2xl flex items-center justify-center">
              <svg class="w-8 h-8 text-green-400" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 19v-6a2 2 0 00-2-2H5a2 2 0 00-2 2v6a2 2 0 002 2h2a2 2 0 002-2zm0 0V9a2 2 0 012-2h2a2 2 0 012 2v10m-6 0a2 2 0 002 2h2a2 2 0 002-2m0 0V5a2 2 0 012-2h2a2 2 0 012 2v14a2 2 0 01-2 2h-2a2 2 0 01-2-2z"></path>
              </svg>
            </div>
            <h3 class="text-2xl font-bold text-white mb-4">数据分析</h3>
            <p class="text-gray-200 leading-relaxed">实时数据分析，直观展示业务状况，辅助决策制定。多维度数据可视化，助力企业精准决策。</p>
          </div>
        </div>
      </div>
    </div>

    <!-- 装饰效果 -->
    <div class="absolute -left-20 top-1/3 w-96 h-96 bg-blue-500/20 rounded-full filter blur-[120px] mix-blend-overlay"></div>
    <div class="absolute -right-20 bottom-1/3 w-96 h-96 bg-purple-500/20 rounded-full filter blur-[120px] mix-blend-overlay"></div>
  </section>
</template>

<script setup>
// 移除 GSAP 相关的导入和初始化代码
</script>

<style scoped>
.gradient-text {
  @apply bg-gradient-to-r from-primary-500 to-secondary-500 bg-clip-text text-transparent;
}
</style> 