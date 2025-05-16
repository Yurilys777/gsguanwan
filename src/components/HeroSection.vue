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
          <a href="#contact" 
             class="group relative px-8 py-4 text-lg font-medium rounded-lg overflow-hidden bg-gradient-to-r from-blue-500 to-purple-500 text-white transform hover:scale-105 transition-all duration-300">
            <div class="absolute inset-0 bg-white/20 group-hover:bg-white/30 transition-colors duration-300"></div>
            <span class="relative flex items-center">
              免费试用
              <svg class="w-5 h-5 ml-2 transform group-hover:translate-x-1 transition-transform duration-300" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M13 7l5 5m0 0l-5 5m5-5H6"></path>
              </svg>
            </span>
          </a>
          
          <a href="#features" 
             class="group px-8 py-4 text-lg font-medium rounded-lg text-gray-300 bg-white/5 hover:bg-white/10 backdrop-blur-sm border border-white/10 transform hover:scale-105 transition-all duration-300">
            了解更多
          </a>
        </div>
        
        <div class="flex items-center justify-center space-x-8 mt-12">
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
import { onMounted } from 'vue'
import gsap from 'gsap'

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
</style> 