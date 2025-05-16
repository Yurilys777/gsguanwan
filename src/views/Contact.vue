<template>
  <div class="relative min-h-screen py-32 px-4 sm:px-6 lg:px-8">
    <!-- 背景特效 -->
    <div class="fixed inset-0 z-0">
      <falling-stars-background
        color="255, 255, 255"
        :count="130"
        :speed="1.6"
        :trailLength="23"
      />
    </div>
    
    <!-- 页面内容 -->
    <div class="relative z-10 max-w-7xl mx-auto">
      <div class="text-center mb-16">
        <h1 class="text-4xl sm:text-5xl font-bold mb-4">
          <span class="text-transparent bg-clip-text bg-gradient-to-r from-blue-500 to-purple-500">
            联系我们
          </span>
        </h1>
        <p class="text-lg text-white/60 max-w-2xl mx-auto">随时为您提供专业的技术支持和服务</p>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
        <!-- 联系表单 -->
        <div class="bg-gray-800/50 backdrop-blur-xl rounded-2xl p-8 border border-gray-700/50">
          <h2 class="text-2xl font-semibold text-white mb-6">发送消息</h2>
          <form class="space-y-6">
            <div>
              <label for="name" class="block text-sm font-medium text-gray-300">姓名</label>
              <input type="text" id="name" name="name" class="mt-1 block w-full rounded-lg border border-gray-700 bg-gray-900/50 text-gray-300 px-4 py-2 focus:outline-none focus:ring-2 focus:ring-blue-500">
            </div>
            <div>
              <label for="email" class="block text-sm font-medium text-gray-300">邮箱</label>
              <input type="email" id="email" name="email" class="mt-1 block w-full rounded-lg border border-gray-700 bg-gray-900/50 text-gray-300 px-4 py-2 focus:outline-none focus:ring-2 focus:ring-blue-500">
            </div>
            <div>
              <label for="message" class="block text-sm font-medium text-gray-300">消息</label>
              <textarea id="message" name="message" rows="4" class="mt-1 block w-full rounded-lg border border-gray-700 bg-gray-900/50 text-gray-300 px-4 py-2 focus:outline-none focus:ring-2 focus:ring-blue-500"></textarea>
            </div>
            <button type="submit" class="w-full px-4 py-2 bg-gradient-to-r from-blue-500 to-purple-500 hover:from-blue-600 hover:to-purple-600 text-white rounded-lg">
              发送
            </button>
          </form>
        </div>

        <!-- 联系信息 -->
        <div class="space-y-8">
          <div class="bg-gray-800/50 backdrop-blur-xl rounded-2xl p-8 border border-gray-700/50">
            <h3 class="text-xl font-semibold text-white mb-4">公司地址</h3>
            <p class="text-gray-300">东莞市周屋基村小雅立创大厦1号楼402</p>
          </div>
          <div class="bg-gray-800/50 backdrop-blur-xl rounded-2xl p-8 border border-gray-700/50">
            <h3 class="text-xl font-semibold text-white mb-4">联系方式</h3>
            <div class="space-y-2">
              <p class="text-gray-300">电话：400-999-8794</p>
              <p class="text-gray-300">邮箱：contact@smartoa.com</p>
            </div>
          </div>
          <div class="bg-gray-800/50 backdrop-blur-xl rounded-2xl p-8 border border-gray-700/50">
            <h3 class="text-xl font-semibold text-white mb-4">工作时间</h3>
            <p class="text-gray-300">周一至周五：9:00 - 18:00</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import FallingStarsBackground from '../components/FallingStarsBackground.vue'
</script> 