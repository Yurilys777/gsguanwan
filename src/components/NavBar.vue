<template>
  <nav class="fixed top-0 left-0 right-0 z-50 bg-gray-900/80 backdrop-blur-md border-b border-gray-800">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="flex items-center justify-between h-16">
        <!-- Logo -->
        <div class="flex-shrink-0">
          <router-link to="/" class="text-2xl font-bold">
            <span class="bg-gradient-to-r from-blue-400 via-purple-400 to-pink-400 text-transparent bg-clip-text font-extrabold tracking-wider hover:from-blue-500 hover:via-purple-500 hover:to-pink-500 transition-all duration-300">
              AutoSmartOA
            </span>
          </router-link>
        </div>

        <!-- 导航链接 -->
        <div class="hidden md:block">
          <div class="ml-10 flex items-center space-x-8">
            <router-link 
              v-for="(item, index) in navItems" 
              :key="index"
              :to="item.path"
              class="text-gray-300 hover:text-white px-3 py-2 rounded-md text-sm font-medium transition-colors duration-200"
              :class="{ 'text-white bg-gray-800': isRouteActive(item.path) }"
            >
              {{ item.name }}
            </router-link>
          </div>
        </div>

        <!-- 登录注册按钮 -->
        <div class="hidden md:flex items-center space-x-4">
          <router-link 
            to="/login"
            class="text-gray-300 hover:text-white px-3 py-2 rounded-md text-sm font-medium transition-colors duration-200"
          >
            登录
          </router-link>
          <router-link 
            to="/register"
            class="bg-gradient-to-r from-blue-500 to-purple-500 hover:from-blue-600 hover:to-purple-600 text-white px-4 py-2 rounded-md text-sm font-medium transition-all duration-200 transform hover:scale-105"
          >
            注册
          </router-link>
        </div>

        <!-- 移动端菜单按钮 -->
        <div class="md:hidden flex items-center">
          <button 
            @click="isOpen = !isOpen"
            class="text-gray-300 hover:text-white p-2"
          >
            <svg 
              class="h-6 w-6" 
              fill="none" 
              viewBox="0 0 24 24" 
              stroke="currentColor"
            >
              <path 
                v-if="!isOpen"
                stroke-linecap="round" 
                stroke-linejoin="round" 
                stroke-width="2" 
                d="M4 6h16M4 12h16M4 18h16"
              />
              <path 
                v-else
                stroke-linecap="round" 
                stroke-linejoin="round" 
                stroke-width="2" 
                d="M6 18L18 6M6 6l12 12"
              />
            </svg>
          </button>
        </div>
      </div>

      <!-- 移动端菜单 -->
      <div 
        v-show="isOpen" 
        class="md:hidden"
      >
        <div class="px-2 pt-2 pb-3 space-y-1">
          <router-link 
            v-for="(item, index) in navItems" 
            :key="index"
            :to="item.path"
            class="block px-3 py-2 rounded-md text-base font-medium text-gray-300 hover:text-white hover:bg-gray-800 transition-colors duration-200"
            :class="{ 'text-white bg-gray-800': isRouteActive(item.path) }"
            @click="isOpen = false"
          >
            {{ item.name }}
          </router-link>
          <!-- 移动端登录注册按钮 -->
          <div class="mt-4 space-y-2">
            <router-link 
              to="/login"
              class="block px-3 py-2 rounded-md text-base font-medium text-gray-300 hover:text-white hover:bg-gray-800 transition-colors duration-200"
              @click="isOpen = false"
            >
              登录
            </router-link>
            <router-link 
              to="/register"
              class="block bg-gradient-to-r from-blue-500 to-purple-500 hover:from-blue-600 hover:to-purple-600 text-white px-4 py-2 rounded-md text-base font-medium transition-all duration-200"
              @click="isOpen = false"
            >
              注册
            </router-link>
          </div>
        </div>
      </div>
    </div>
  </nav>
</template>

<script setup>
import { ref } from 'vue'
import { useRoute } from 'vue-router'

const route = useRoute()
const isOpen = ref(false)

const navItems = [
  { name: '首页', path: '/' },
  { name: '关于我们', path: '/about' },
  { name: '服务', path: '/services' },
  { name: '解决方案', path: '/solutions' },
  { name: '产品', path: '/products' },
  { name: '联系我们', path: '/contact' }
]

const isRouteActive = (path) => {
  return route.path === path
}
</script>

<style scoped>
/* 添加渐变动画 */
@keyframes gradient {
  0% {
    background-position: 0% 50%;
  }
  50% {
    background-position: 100% 50%;
  }
  100% {
    background-position: 0% 50%;
  }
}
</style> 