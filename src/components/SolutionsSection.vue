<template>
  <section class="relative py-24 overflow-hidden">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="text-center mb-16">
        <h2 class="text-4xl sm:text-5xl font-bold mb-4">
          <span class="text-transparent bg-clip-text bg-gradient-to-r from-blue-500 to-purple-500">
            解决方案
          </span>
        </h2>
        <p class="text-xl text-gray-300">为不同规模企业提供定制化的智能办公解决方案</p>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
        <!-- 中小企业解决方案 -->
        <div class="group relative p-8 bg-gray-800/90 backdrop-blur-sm rounded-2xl border border-gray-700 hover:border-blue-500 transition-all duration-300 hover:-translate-y-2">
          <div class="absolute inset-0 bg-gradient-to-br from-blue-500/30 to-purple-500/30 rounded-2xl opacity-0 group-hover:opacity-100 transition-opacity duration-300"></div>
          <div class="relative">
            <div class="w-16 h-16 mb-6 bg-blue-500/30 rounded-2xl flex items-center justify-center">
              <svg class="w-8 h-8 text-blue-400" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 21V5a2 2 0 00-2-2H7a2 2 0 00-2 2v16m14 0h2m-2 0h-5m-9 0H3m2 0h5M9 7h1m-1 4h1m4-4h1m-1 4h1m-5 10v-5a1 1 0 011-1h2a1 1 0 011 1v5m-4 0h4"></path>
              </svg>
            </div>
            <h3 class="text-2xl font-bold text-white mb-4">中小企业解决方案</h3>
            <ul class="space-y-3">
              <li class="flex items-center text-gray-200">
                <svg class="w-5 h-5 text-green-400 mr-3" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7"></path>
                </svg>
                <span>快速部署，即开即用</span>
              </li>
              <li class="flex items-center text-gray-200">
                <svg class="w-5 h-5 text-green-400 mr-3" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7"></path>
                </svg>
                <span>成本可控，按需付费</span>
              </li>
              <li class="flex items-center text-gray-200">
                <svg class="w-5 h-5 text-green-400 mr-3" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7"></path>
                </svg>
                <span>简单易用，无需培训</span>
              </li>
            </ul>
          </div>
        </div>

        <!-- 大型企业解决方案 -->
        <div class="group relative p-8 bg-gray-800/90 backdrop-blur-sm rounded-2xl border border-gray-700 hover:border-purple-500 transition-all duration-300 hover:-translate-y-2">
          <div class="absolute inset-0 bg-gradient-to-br from-purple-500/30 to-pink-500/30 rounded-2xl opacity-0 group-hover:opacity-100 transition-opacity duration-300"></div>
          <div class="relative">
            <div class="w-16 h-16 mb-6 bg-purple-500/30 rounded-2xl flex items-center justify-center">
              <svg class="w-8 h-8 text-purple-400" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 21V5a2 2 0 00-2-2H7a2 2 0 00-2 2v16m14 0h2m-2 0h-5m-9 0H3m2 0h5M9 7h1m-1 4h1m4-4h1m-1 4h1m-5 10v-5a1 1 0 011-1h2a1 1 0 011 1v5m-4 0h4"></path>
              </svg>
            </div>
            <h3 class="text-2xl font-bold text-white mb-4">大型企业解决方案</h3>
            <ul class="space-y-3">
              <li class="flex items-center text-gray-200">
                <svg class="w-5 h-5 text-green-400 mr-3" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7"></path>
                </svg>
                <span>私有化部署，数据安全</span>
              </li>
              <li class="flex items-center text-gray-200">
                <svg class="w-5 h-5 text-green-400 mr-3" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7"></path>
                </svg>
                <span>定制化开发，满足特殊需求</span>
              </li>
              <li class="flex items-center text-gray-200">
                <svg class="w-5 h-5 text-green-400 mr-3" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7"></path>
                </svg>
                <span>全方位技术支持</span>
              </li>
            </ul>
          </div>
        </div>
      </div>
      
      <!-- Safari浏览器模型展示区域 -->
      <div class="mt-32">
        <h2 class="text-4xl sm:text-5xl font-bold mb-4 text-center">
          <span class="text-transparent bg-clip-text bg-gradient-to-r from-blue-500 to-purple-500">
            PC端界面展示
          </span>
        </h2>
        <p class="text-xl text-gray-300 mb-12 text-center">高效直观的操作界面，提升企业办公流程管理效率</p>
        
        <div class="flex justify-center">
          <div class="w-full max-w-5xl transform hover:scale-[1.02] transition-transform duration-300">
            <SafariMockup 
              :width="1000" 
              :height="625" 
              url="https://autosmartoa.com/dashboard"
            />
          </div>
        </div>
      </div>
      
      <!-- iPhone 模型展示区域 -->
      <div class="mt-24">
        <h2 class="text-4xl sm:text-5xl font-bold mb-4 text-center">
          <span class="text-transparent bg-clip-text bg-gradient-to-r from-blue-500 to-purple-500">
            移动应用展示
          </span>
        </h2>
        <p class="text-xl text-gray-300 mb-12 text-center">随时随地管理工作，让办公不再受时间和空间限制</p>
        
        <div class="flex flex-col md:flex-row justify-center items-center gap-12 flex-wrap">
          <!-- 第一个iPhone展示 -->
          <div class="flex flex-col items-center transform hover:scale-[1.02] transition-transform duration-300">
            <iPhone15ProMockup 
              :width="300" 
              :height="610" 
              src="/images/app-screen-1.jpg"
            />
            <h3 class="text-xl font-semibold text-white mt-6">智能工作台</h3>
            <p class="text-gray-300 mt-2 text-center max-w-xs">个性化工作台，数据一目了然</p>
          </div>
          
          <!-- 第二个iPhone展示 -->
          <div class="flex flex-col items-center transform hover:scale-[1.02] transition-transform duration-300">
            <iPhone15ProMockup 
              :width="300" 
              :height="610" 
              src="/images/app-screen-2.jpg"
            />
            <h3 class="text-xl font-semibold text-white mt-6">任务协作</h3>
            <p class="text-gray-300 mt-2 text-center max-w-xs">团队协作更高效，任务跟踪一步到位</p>
          </div>
          
          <!-- 第三个iPhone展示 -->
          <div class="flex flex-col items-center transform hover:scale-[1.02] transition-transform duration-300">
            <iPhone15ProMockup 
              :width="300" 
              :height="610" 
              src="/images/app-screen-3.jpg"
            />
            <h3 class="text-xl font-semibold text-white mt-6">数据分析</h3>
            <p class="text-gray-300 mt-2 text-center max-w-xs">数据可视化，助力企业决策</p>
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
import SafariMockup from './SafariMockup.vue'
import iPhone15ProMockup from './iPhone15ProMockup.vue'
</script>

<style scoped>
.gradient-text {
  @apply bg-gradient-to-r from-primary-500 to-secondary-500 bg-clip-text text-transparent;
}
</style> 