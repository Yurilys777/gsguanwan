<template>
  <section class="relative min-h-screen flex items-center py-20 overflow-hidden">
    <!-- 背景渐变 -->
    <div class="absolute inset-0 bg-gradient-radial from-blue-500/10 via-purple-500/5 to-transparent"></div>
    
    <div class="relative container mx-auto px-4 sm:px-6 lg:px-8 z-10">
      <div class="text-center max-w-4xl mx-auto">
        <h1 class="text-5xl md:text-7xl font-bold mb-8">
          <span class="inline-block text-transparent bg-clip-text bg-gradient-to-r from-blue-400 via-purple-400 to-pink-400 animate-text-shimmer">
            自动化OA管理系统
          </span>
        </h1>
        
        <p class="text-xl md:text-2xl text-gray-300 mb-12 leading-relaxed">
          采用<span class="text-blue-400 font-semibold">AI驱动</span>的新一代办公系统
          <br>打造智能化、自动化的办公环境
        </p>
        
        <div class="flex flex-col sm:flex-row items-center justify-center gap-4">
          <div class="relative">
            <button 
              @click="toggleDownloadOptions"
              class="group relative px-8 py-4 text-lg font-medium rounded-lg overflow-hidden bg-gradient-to-r from-blue-500 to-purple-500 text-white transform hover:scale-105 transition-all duration-300"
            >
              <div class="absolute inset-0 bg-white/20 group-hover:bg-white/30 transition-colors duration-300"></div>
              <span class="relative flex items-center">
                免费试用
                <svg 
                  class="w-5 h-5 ml-2 transition-transform duration-300" 
                  :class="showDownloadOptions ? 'rotate-180' : ''" 
                  fill="none" 
                  stroke="currentColor" 
                  viewBox="0 0 24 24"
                >
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7"></path>
                </svg>
              </span>
            </button>
          </div>
          
          <a href="#features" 
             class="group px-8 py-4 text-lg font-medium rounded-lg text-gray-300 bg-white/5 hover:bg-white/10 backdrop-blur-sm border border-white/10 transform hover:scale-105 transition-all duration-300">
            了解更多
          </a>
        </div>
        
        <!-- 下载选项展开区域 - 固定位置 -->
        <div 
          v-show="showDownloadOptions" 
          class="fixed top-1/2 right-10 -translate-y-1/2 w-80 rounded-lg bg-gray-800/95 backdrop-blur-xl p-5 z-50 shadow-2xl border border-blue-500/30 transition-all duration-500 transform"
          :class="showDownloadOptions ? 'scale-100 opacity-100 translate-x-0' : 'scale-90 opacity-0 translate-x-20'"
        >
          <div class="flex justify-between items-center mb-4 border-b border-gray-700/50 pb-3">
            <h3 class="text-lg font-medium text-white">选择下载平台</h3>
            <button 
              @click="toggleDownloadOptions"
              class="text-gray-400 hover:text-white rounded-full p-1 hover:bg-gray-700/50 transition-colors"
            >
              <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12"></path>
              </svg>
            </button>
          </div>
          
          <div class="grid grid-cols-1 gap-3 max-h-[calc(100vh-200px)] overflow-y-auto py-1 custom-scrollbar">
            <InteractiveHoverButton 
              v-for="(option, index) in downloadOptions" 
              :key="index" 
              :text="option.name" 
              :platform="option.platform"
              @click="downloadApp(option.url)" 
            />
            
            <div class="flex items-center space-x-3 mt-3 pt-3 border-t border-gray-700/50">
              <div class="flex items-center text-yellow-400">
                <svg class="w-5 h-5" fill="currentColor" viewBox="0 0 20 20">
                  <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z"></path>
                </svg>
                <span class="ml-1">4.9/5</span>
              </div>
              <div class="flex items-center text-green-400">
                <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z"></path>
                </svg>
                <span class="ml-1">企业认证</span>
              </div>
            </div>
          </div>
        </div>
        
        <div class="flex items-center justify-center space-x-8 mt-12 relative z-10">
          <div class="flex items-center text-gray-300">
            <svg class="w-5 h-5 text-yellow-400" fill="currentColor" viewBox="0 0 20 20">
              <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.72c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z"></path>
            </svg>
            <span class="ml-2">4.9/5 用户评分</span>
          </div>
          
          <div class="flex items-center text-gray-300">
            <svg class="w-5 h-5 text-green-400" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z"></path>
            </svg>
            <span class="ml-2">企业认证</span>
          </div>
        </div>
      </div>
    </div>
    
    <!-- 装饰效果 -->
    <div class="absolute left-0 top-1/4 w-72 h-72 bg-blue-500/30 rounded-full filter blur-[100px] animate-blob"></div>
    <div class="absolute right-0 bottom-1/4 w-72 h-72 bg-purple-500/30 rounded-full filter blur-[100px] animate-blob animation-delay-2000"></div>
  </section>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from 'vue'
import gsap from 'gsap'
import InteractiveHoverButton from './InteractiveHoverButton.vue'

const showDownloadOptions = ref(false)

const downloadOptions = [
  { name: '安卓端下载', url: '/downloads/android', platform: 'android' },
  { name: '苹果端下载', url: '/downloads/ios', platform: 'ios' },
  { name: 'PC端下载', url: '/downloads/windows', platform: 'windows' },
  { name: 'Linux端下载', url: '/downloads/linux', platform: 'linux' },
  { name: '小程序', url: '/miniprogram', platform: 'miniprogram' }
]

const toggleDownloadOptions = () => {
  showDownloadOptions.value = !showDownloadOptions.value
  
  // 根据菜单状态为内容添加动画
  if (showDownloadOptions.value) {
    // 展开菜单时，按钮逐个淡入
    gsap.fromTo('.grid.grid-cols-1.gap-3 > *', 
      { y: 20, opacity: 0, scale: 0.9 },
      { 
        y: 0, 
        opacity: 1, 
        scale: 1,
        duration: 0.3, 
        stagger: 0.08,
        ease: 'back.out(1.2)'
      }
    )
    
    // 隐藏底部评分区域
    gsap.to('.flex.items-center.justify-center.space-x-8', {
      opacity: 0.3,
      duration: 0.3
    })
  } else {
    // 显示底部评分区域
    gsap.to('.flex.items-center.justify-center.space-x-8', {
      opacity: 1,
      duration: 0.3
    })
  }
}

const downloadApp = (url) => {
  // 实际下载逻辑
  console.log('下载应用:', url)
  // 可以将window.location.href = url 或使用其他下载方法
}

// 点击外部关闭下拉菜单
const handleClickOutside = (event) => {
  const downloadButton = document.querySelector('.group.relative')
  if (downloadButton && !downloadButton.contains(event.target) && showDownloadOptions.value) {
    showDownloadOptions.value = false
  }
}

onMounted(() => {
  gsap.from('h1', {
    opacity: 0,
    y: 50,
    duration: 1,
    ease: 'power3.out'
  })
  
  gsap.from('p', {
    opacity: 0,
    y: 30,
    duration: 1,
    delay: 0.3,
    ease: 'power3.out'
  })
  
  gsap.from('.flex', {
    opacity: 0,
    y: 30,
    duration: 1,
    delay: 0.6,
    ease: 'power3.out'
  })
  
  document.addEventListener('click', handleClickOutside)
})

onUnmounted(() => {
  document.removeEventListener('click', handleClickOutside)
})
</script>

<style scoped>
.animate-text-shimmer {
  background-size: 200% 200%;
  animation: text-shimmer 3s linear infinite;
}

@keyframes text-shimmer {
  0% { background-position: 200% 50%; }
  100% { background-position: -200% 50%; }
}

.animation-delay-2000 {
  animation-delay: 2s;
}

.animate-blob {
  animation: blob 7s infinite;
}

@keyframes blob {
  0% {
    transform: translate(0px, 0px) scale(1);
  }
  33% {
    transform: translate(30px, -50px) scale(1.1);
  }
  66% {
    transform: translate(-20px, 20px) scale(0.9);
  }
  100% {
    transform: translate(0px, 0px) scale(1);
  }
}

.transform {
  transition-property: transform, opacity, translate;
  transition-timing-function: cubic-bezier(0.4, 0, 0.2, 1);
  transition-duration: 300ms;
}

/* 隐藏滚动条但保留滚动功能 */
.custom-scrollbar {
  scrollbar-width: none; /* Firefox */
  -ms-overflow-style: none; /* IE and Edge */
}

.custom-scrollbar::-webkit-scrollbar {
  display: none; /* Chrome, Safari and Opera */
}

/* 增强下拉菜单阴影发光效果 */
.shadow-2xl {
  box-shadow: 0 0 30px rgba(59, 130, 246, 0.4), 
              0 0 50px rgba(139, 92, 246, 0.2);
}

/* 覆盖全屏的遮罩层 - 可选添加 */
.fixed:before {
  content: '';
  position: fixed;
  inset: 0;
  background: rgba(0, 0, 0, 0.5);
  backdrop-filter: blur(2px);
  z-index: -1;
  opacity: 0;
  transition: opacity 0.3s ease;
}

.fixed[v-show="true"]:before {
  opacity: 1;
}
</style> 