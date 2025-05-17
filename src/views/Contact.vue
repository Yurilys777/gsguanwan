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
          <form class="space-y-6" @submit.prevent="handleSubmit">
            <div>
              <label for="name" class="block text-sm font-medium text-gray-300">姓名</label>
              <input type="text" id="name" v-model="formData.name" name="name" class="mt-1 block w-full rounded-lg border border-gray-700 bg-gray-900/50 text-gray-300 px-4 py-2 focus:outline-none focus:ring-2 focus:ring-blue-500">
            </div>
            <div>
              <label for="email" class="block text-sm font-medium text-gray-300">邮箱</label>
              <input type="email" id="email" v-model="formData.email" name="email" class="mt-1 block w-full rounded-lg border border-gray-700 bg-gray-900/50 text-gray-300 px-4 py-2 focus:outline-none focus:ring-2 focus:ring-blue-500">
            </div>
            <div>
              <label for="message" class="block text-sm font-medium text-gray-300">消息</label>
              <textarea id="message" v-model="formData.message" name="message" rows="4" class="mt-1 block w-full rounded-lg border border-gray-700 bg-gray-900/50 text-gray-300 px-4 py-2 focus:outline-none focus:ring-2 focus:ring-blue-500"></textarea>
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
  
  <!-- 通知弹窗 (模态框样式) -->
  <div v-if="showNotification" class="fixed inset-0 flex items-center justify-center z-[9999]">
    <div class="absolute inset-0 bg-black/60 backdrop-blur-sm" @click="showNotification = false"></div>
    <div class="bg-gray-800/90 backdrop-blur-xl border border-gray-700/50 text-white px-8 py-6 rounded-2xl shadow-2xl z-10 max-w-md mx-auto transform scale-100 transition-all duration-300 ease-in-out">
      <div class="flex items-center mb-4">
        <div class="w-10 h-10 rounded-full bg-gradient-to-r from-blue-500 to-purple-500 flex items-center justify-center mr-3">
          <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6 text-white" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
          </svg>
        </div>
        <h3 class="text-xl font-bold text-transparent bg-clip-text bg-gradient-to-r from-blue-400 to-purple-400">提交成功</h3>
      </div>
      <p class="text-gray-300 mb-5">{{ notificationMessage }}</p>
      <button @click="showNotification = false" class="w-full px-4 py-2 bg-gradient-to-r from-blue-500 to-purple-500 hover:from-blue-600 hover:to-purple-600 text-white rounded-lg transition-all duration-200">
        确定
      </button>
    </div>
  </div>
</template>

<script setup>
import FallingStarsBackground from '../components/FallingStarsBackground.vue'
import { ref, reactive } from 'vue'

// 表单数据
const formData = reactive({
  name: '',
  email: '',
  message: ''
})

// 通知状态
const showNotification = ref(false)
const notificationMessage = ref('')

// 提交表单
const handleSubmit = () => {
  console.log('表单提交开始')
  
  // 显示成功通知
  notificationMessage.value = '消息已发送，我们会尽快回复您！'
  showNotification.value = true
  console.log('设置通知状态:', showNotification.value)
  
  // 清空表单
  formData.name = ''
  formData.email = ''
  formData.message = ''
}
</script>

<style scoped>
/* 添加一些额外的动画效果 */
.transform {
  transition: all 0.3s ease-in-out;
}

@keyframes modalFadeIn {
  from {
    opacity: 0;
    transform: scale(0.9);
  }
  to {
    opacity: 1;
    transform: scale(1);
  }
}

.fixed.inset-0 {
  animation: modalFadeIn 0.3s ease-out forwards;
}
</style>