<template>
  <nav class="fixed top-0 left-0 right-0 w-full z-[9999999] bg-gray-900/95 backdrop-blur-md border-b border-gray-800 shadow-lg">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="flex items-center justify-between h-16">
        <!-- Logo (靠左) -->
        <div class="flex-shrink-0 w-1/4">
          <router-link to="/" class="text-2xl font-bold">
            <span class="bg-gradient-to-r from-blue-400 via-purple-400 to-pink-400 text-transparent bg-clip-text font-extrabold tracking-wider hover:from-blue-500 hover:via-purple-500 hover:to-pink-500 transition-all duration-300">
              AutoSmartOA
            </span>
          </router-link>
        </div>

        <!-- 导航链接 (居中) -->
        <div class="hidden md:flex justify-center w-2/4">
          <div class="flex items-center justify-center space-x-6">
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

        <!-- 右侧功能区 -->
        <div class="hidden md:flex items-center justify-end w-1/4 space-x-6">
          <!-- 搜索图标 -->
          <button 
            @click="handleSearchClick" 
            class="text-gray-300 hover:text-white transition-colors duration-200"
          >
            <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z"></path>
            </svg>
          </button>
          
          <!-- 客服热线 -->
          <div class="flex items-center text-gray-300">
            <svg class="w-4 h-4 mr-2" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 5a2 2 0 012-2h3.28a1 1 0 01.948.684l1.498 4.493a1 1 0 01-.502 1.21l-2.257 1.13a11.042 11.042 0 005.516 5.516l1.13-2.257a1 1 0 011.21-.502l4.493 1.498a1 1 0 01.684.949V19a2 2 0 01-2 2h-1C9.716 21 3 14.284 3 6V5z"></path>
            </svg>
            <span class="text-xs">400-999-8794</span>
          </div>
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
          
          <!-- 移动端显示客服热线 -->
          <div class="flex items-center text-gray-300 px-3 py-2">
            <svg class="w-4 h-4 mr-2" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 5a2 2 0 012-2h3.28a1 1 0 01.948.684l1.498 4.493a1 1 0 01-.502 1.21l-2.257 1.13a11.042 11.042 0 005.516 5.516l1.13-2.257a1 1 0 011.21-.502l4.493 1.498a1 1 0 01.684.949V19a2 2 0 01-2 2h-1C9.716 21 3 14.284 3 6V5z"></path>
            </svg>
            <span class="text-xs">400-888-9999</span>
          </div>
        </div>
      </div>
    </div>
  </nav>
  
  <!-- 全屏搜索框 -->
  <div 
    v-if="searchVisible" 
    class="fixed inset-0 bg-black/70 backdrop-blur-sm flex items-center justify-center z-[9999] transition-opacity duration-300"
    @click="closeSearch"
  >
    <div 
      class="max-w-2xl w-full mx-4 transform transition-all duration-300 scale-search scale-100"
      @click.stop
    >
      <form @submit.prevent="handleSearch" class="relative">
        <div class="relative">
          <input 
            ref="searchInput"
            v-model="searchQuery" 
            type="text" 
            placeholder="输入关键词搜索..." 
            class="w-full bg-gray-800/80 backdrop-blur-xl text-white text-lg px-6 py-4 pr-14 rounded-xl border border-gray-700/50 shadow-2xl focus:outline-none focus:ring-2 focus:ring-blue-500/50 transition-all"
            @keydown.esc="closeSearch"
          />
          <button 
            type="submit"
            class="absolute right-2 top-1/2 transform -translate-y-1/2 bg-gradient-to-r from-blue-500 to-purple-500 hover:from-blue-600 hover:to-purple-600 text-white p-2 rounded-lg transition-all duration-200"
          >
            <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z"></path>
            </svg>
          </button>
        </div>
        <div class="text-gray-400 text-sm mt-2 text-center">按 ESC 键关闭</div>
      </form>
    </div>
  </div>
</template>

<script setup>
import { ref, nextTick, onMounted, onBeforeUnmount } from 'vue'
import { useRoute, useRouter } from 'vue-router'

const route = useRoute()
const router = useRouter()
const isOpen = ref(false)
const searchVisible = ref(false)
const searchQuery = ref('')
const searchInput = ref(null)

const navItems = [
  { name: '首页', path: '/' },
  { name: '关于我们', path: '/about' },
  { name: '技术服务', path: '/services' },
  { name: '解决方案', path: '/solutions' },
  { name: '产品功能', path: '/products' },
  { name: '联系我们', path: '/contact' }
]

// 搜索相关功能
const handleSearchClick = () => {
  console.log('Search button clicked')
  searchVisible.value = true
  document.body.style.overflow = 'hidden'
  
  // 等待DOM更新后聚焦输入框
  nextTick(() => {
    console.log('Focusing search input')
    searchInput.value?.focus()
  })
}

const closeSearch = () => {
  console.log('Closing search')
  searchVisible.value = false
  document.body.style.overflow = ''
}

const handleSearch = () => {
  console.log('Search submitted:', searchQuery.value)
  if (searchQuery.value.trim()) {
    // 这里可以添加实际的搜索逻辑，现在只是跳转到首页
    router.push('/')
    
    // 重置搜索框
    searchQuery.value = ''
    closeSearch()
  }
}

// 添加ESC键关闭搜索框
const handleEscKey = (event) => {
  if (event.key === 'Escape' && searchVisible.value) {
    closeSearch()
  }
}

// 组件生命周期钩子 - 确保事件监听器的添加和移除
onMounted(() => {
  document.addEventListener('keydown', handleEscKey)
})

onBeforeUnmount(() => {
  document.removeEventListener('keydown', handleEscKey)
  // 确保离开页面时恢复滚动
  document.body.style.overflow = ''
})

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

/* 搜索框动画 */
.scale-search {
  transition: all 0.3s cubic-bezier(0.34, 1.56, 0.64, 1);
}

.scale-100 {
  transform: scale(1);
}

.scale-95 {
  transform: scale(0.95);
}

.opacity-100 {
  opacity: 1;
}

.opacity-0 {
  opacity: 0;
}
</style>

<style>
/* 隐藏默认滚动条 - 适用于Webkit浏览器(Chrome, Safari, Edge) */
::-webkit-scrollbar {
  width: 6px;
  height: 6px;
}

::-webkit-scrollbar-track {
  background: rgba(0, 0, 0, 0.2);
  border-radius: 20px;
  backdrop-filter: blur(5px);
  -webkit-backdrop-filter: blur(5px);
}

::-webkit-scrollbar-thumb {
  background-color: rgba(255, 255, 255, 0.05);
  border-radius: 20px;
  transition: background-color 0.3s;
  backdrop-filter: blur(10px);
  -webkit-backpack-filter: blur(10px);
  border: 1px solid rgba(255, 255, 255, 0.05);
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);
}

::-webkit-scrollbar-thumb:hover {
  background-color: rgba(255, 255, 255, 0.1);
}

/* 隐藏默认滚动条 - Firefox */
* {
  scrollbar-width: thin;
  scrollbar-color: rgba(255, 255, 255, 0.05) rgba(0, 0, 0, 0.2);
}

/* 增强沉浸感的其他样式 */
html, body {
  overflow-x: hidden; /* 防止水平滚动条 */
  scroll-behavior: smooth; /* 平滑滚动 */
}

/* 为页面添加自定义滚动容器样式 - 类似"了解更多"按钮风格 */
.custom-scroll-container {
  scrollbar-gutter: stable;
}
</style>