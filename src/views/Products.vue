<template>
  <div class="relative min-h-screen py-32 px-4 sm:px-6 lg:px-8">
    <!-- 背景特效 -->
    <div class="fixed inset-0 z-0">
      <falling-stars-background
        color="255, 255, 255"
        :count="135"
        :speed="1.9"
        :trailLength="21"
      />
    </div>
    
    <!-- 页面内容 -->
    <div class="relative z-10 max-w-7xl mx-auto">
      <div class="text-center mb-16">
        <h1 class="text-4xl sm:text-5xl font-bold mb-4">
          <span class="text-transparent bg-clip-text bg-gradient-to-r from-blue-500 to-purple-500">
            产品功能
          </span>
        </h1>
        <p class="text-lg text-white/60 max-w-2xl mx-auto">为您的企业提供全方位的自动化办公解决方案</p>
      </div>

      <!-- 产品卡片网格 -->
      <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
        <!-- 工作流自动化 -->
        <div class="bg-gray-800/50 backdrop-blur-xl rounded-2xl p-8 border border-gray-700/50 hover:border-blue-500/50 transition-colors">
          <div class="w-12 h-12 bg-blue-500/20 rounded-lg flex items-center justify-center mb-4">
            <svg class="w-6 h-6 text-blue-400" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5H7a2 2 0 00-2 2v12a2 2 0 002 2h10a2 2 0 002-2V7a2 2 0 00-2-2h-2M9 5a2 2 0 002 2h2a2 2 0 002-2M9 5a2 2 0 012-2h2a2 2 0 012 2m-3 7h3m-3 4h3m-6-4h.01M9 16h.01" />
            </svg>
          </div>
          <h3 class="text-xl font-semibold text-white mb-4">工作流自动化</h3>
          <p class="text-gray-300">自定义工作流程，实现业务全流程自动化</p>
          <div class="mt-6 space-y-2">
            <div class="flex items-center text-gray-400">
              <span class="w-32">工作流引擎</span>
              <div class="flex-1 h-2 bg-gray-700 rounded-full">
                <div class="h-2 bg-blue-500 rounded-full" style="width: 90%"></div>
              </div>
            </div>
            <div class="flex items-center text-gray-400">
              <span class="w-32">表单设计器</span>
              <div class="flex-1 h-2 bg-gray-700 rounded-full">
                <div class="h-2 bg-blue-500 rounded-full" style="width: 85%"></div>
              </div>
            </div>
            <div class="flex items-center text-gray-400">
              <span class="w-32">流程监控</span>
              <div class="flex-1 h-2 bg-gray-700 rounded-full">
                <div class="h-2 bg-blue-500 rounded-full" style="width: 95%"></div>
              </div>
            </div>
          </div>
        </div>

        <!-- 智能文档管理 -->
        <div class="bg-gray-800/50 backdrop-blur-xl rounded-2xl p-8 border border-gray-700/50 hover:border-purple-500/50 transition-colors">
          <div class="w-12 h-12 bg-purple-500/20 rounded-lg flex items-center justify-center mb-4">
            <svg class="w-6 h-6 text-purple-400" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M8 7v8a2 2 0 002 2h6M8 7V5a2 2 0 012-2h4.586a1 1 0 01.707.293l4.414 4.414a1 1 0 01.293.707V15a2 2 0 01-2 2h-2M8 7H6a2 2 0 00-2 2v10a2 2 0 002 2h8a2 2 0 002-2v-2" />
            </svg>
          </div>
          <h3 class="text-xl font-semibold text-white mb-4">智能文档管理</h3>
          <p class="text-gray-300">集中存储和管理企业文档，支持在线协作</p>
          <div class="mt-6 space-y-2">
            <div class="flex items-center text-gray-400">
              <span class="w-32">文档协作</span>
              <div class="flex-1 h-2 bg-gray-700 rounded-full">
                <div class="h-2 bg-purple-500 rounded-full" style="width: 92%"></div>
              </div>
            </div>
            <div class="flex items-center text-gray-400">
              <span class="w-32">版本控制</span>
              <div class="flex-1 h-2 bg-gray-700 rounded-full">
                <div class="h-2 bg-purple-500 rounded-full" style="width: 88%"></div>
              </div>
            </div>
            <div class="flex items-center text-gray-400">
              <span class="w-32">权限管理</span>
              <div class="flex-1 h-2 bg-gray-700 rounded-full">
                <div class="h-2 bg-purple-500 rounded-full" style="width: 94%"></div>
              </div>
            </div>
          </div>
        </div>

        <!-- 数据分析 -->
        <div class="bg-gray-800/50 backdrop-blur-xl rounded-2xl p-8 border border-gray-700/50 hover:border-blue-500/50 transition-colors">
          <div class="w-12 h-12 bg-blue-500/20 rounded-lg flex items-center justify-center mb-4">
            <svg class="w-6 h-6 text-blue-400" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M16 8v8m-4-5v5m-4-2v2m-2 4h12a2 2 0 002-2V6a2 2 0 00-2-2H6a2 2 0 00-2 2v12a2 2 0 002 2z" />
            </svg>
          </div>
          <h3 class="text-xl font-semibold text-white mb-4">数据分析</h3>
          <p class="text-gray-300">强大的数据分析工具，助您洞察业务趋势</p>
          <div class="mt-6 space-y-2">
            <div class="flex items-center text-gray-400">
              <span class="w-32">可视化图表</span>
              <div class="flex-1 h-2 bg-gray-700 rounded-full">
                <div class="h-2 bg-blue-500 rounded-full" style="width: 96%"></div>
              </div>
            </div>
            <div class="flex items-center text-gray-400">
              <span class="w-32">实时监控</span>
              <div class="flex-1 h-2 bg-gray-700 rounded-full">
                <div class="h-2 bg-blue-500 rounded-full" style="width: 89%"></div>
              </div>
            </div>
            <div class="flex items-center text-gray-400">
              <span class="w-32">报表生成</span>
              <div class="flex-1 h-2 bg-gray-700 rounded-full">
                <div class="h-2 bg-blue-500 rounded-full" style="width: 93%"></div>
              </div>
            </div>
          </div>
        </div>
      </div>
      
      <!-- Safari浏览器模型展示区域 -->
      <div class="mt-32">
        <h2 class="text-3xl font-bold text-center mb-4">
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
        <h2 class="text-3xl font-bold text-center mb-4">
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
  </div>
</template>

<script setup>
import FallingStarsBackground from '../components/FallingStarsBackground.vue'
import iPhone15ProMockup from '../components/iPhone15ProMockup.vue'
import SafariMockup from '../components/SafariMockup.vue'
</script> 