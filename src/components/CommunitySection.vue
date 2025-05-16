<template>
  <section class="py-24 bg-white dark:bg-gray-900">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="text-center mb-16">
        <h2 class="text-3xl sm:text-4xl font-bold mb-4">
          <span class="gradient-text">加入我们的社区</span>
        </h2>
        <p class="text-xl text-gray-600 dark:text-gray-400">
          与数千名开发者一起交流学习，分享经验
        </p>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
        <!-- GitHub -->
        <div class="bg-gray-50 dark:bg-gray-800 rounded-xl p-8 text-center hover:shadow-lg transition-all duration-300">
          <div class="w-16 h-16 mx-auto bg-gradient-to-r from-primary-500 to-secondary-500 rounded-full flex items-center justify-center mb-6">
            <svg class="w-8 h-8 text-white" fill="currentColor" viewBox="0 0 24 24">
              <path fill-rule="evenodd" clip-rule="evenodd" d="M12 2C6.477 2 2 6.477 2 12c0 4.42 2.865 8.17 6.839 9.49.5.092.682-.217.682-.482 0-.237-.008-.866-.013-1.7-2.782.604-3.369-1.34-3.369-1.34-.454-1.156-1.11-1.464-1.11-1.464-.908-.62.069-.608.069-.608 1.003.07 1.531 1.03 1.531 1.03.892 1.529 2.341 1.087 2.91.832.092-.647.35-1.088.636-1.338-2.22-.253-4.555-1.11-4.555-4.943 0-1.091.39-1.984 1.029-2.683-.103-.253-.446-1.27.098-2.647 0 0 .84-.269 2.75 1.025A9.578 9.578 0 0112 6.836c.85.004 1.705.114 2.504.336 1.909-1.294 2.747-1.025 2.747-1.025.546 1.377.203 2.394.1 2.647.64.699 1.028 1.592 1.028 2.683 0 3.842-2.339 4.687-4.566 4.935.359.309.678.919.678 1.852 0 1.336-.012 2.415-.012 2.743 0 .267.18.578.688.48C19.138 20.167 22 16.418 22 12c0-5.523-4.477-10-10-10z"/>
            </svg>
          </div>
          <h3 class="text-xl font-semibold text-gray-900 dark:text-white mb-4">GitHub</h3>
          <p class="text-gray-600 dark:text-gray-400 mb-6">在 GitHub 上关注我们的开源项目</p>
          <a href="https://github.com" target="_blank" rel="noopener" class="inline-flex items-center text-primary-500 hover:text-primary-600">
            <span>访问仓库</span>
            <svg class="w-4 h-4 ml-2" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M14 5l7 7m0 0l-7 7m7-7H3"/>
            </svg>
          </a>
        </div>

        <!-- Discord -->
        <div class="bg-gray-50 dark:bg-gray-800 rounded-xl p-8 text-center hover:shadow-lg transition-all duration-300">
          <div class="w-16 h-16 mx-auto bg-gradient-to-r from-primary-500 to-secondary-500 rounded-full flex items-center justify-center mb-6">
            <svg class="w-8 h-8 text-white" fill="currentColor" viewBox="0 0 24 24">
              <path d="M20.317 4.37a19.791 19.791 0 00-4.885-1.515.074.074 0 00-.079.037c-.21.375-.444.864-.608 1.25a18.27 18.27 0 00-5.487 0 12.64 12.64 0 00-.617-1.25.077.077 0 00-.079-.037A19.736 19.736 0 003.677 4.37a.07.07 0 00-.032.027C.533 9.046-.32 13.58.099 18.057a.082.082 0 00.031.057 19.9 19.9 0 005.993 3.03.078.078 0 00.084-.028c.462-.63.874-1.295 1.226-1.994.021-.041.001-.09-.041-.106a13.107 13.107 0 01-1.872-.892.075.075 0 01-.008-.125c.126-.095.252-.193.372-.292a.075.075 0 01.078-.01c3.927 1.793 8.18 1.793 12.061 0a.075.075 0 01.079.01c.12.098.246.198.373.292.044.032.04.1-.006.125-.598.35-1.22.645-1.873.892a.075.075 0 00-.041.106c.36.698.772 1.362 1.225 1.994a.076.076 0 00.084.028 19.834 19.834 0 006.002-3.03.077.077 0 00.032-.054c.5-5.177-.838-9.674-3.549-13.66a.061.061 0 00-.031-.03zM8.02 15.33c-1.183 0-2.157-1.085-2.157-2.419 0-1.333.956-2.419 2.157-2.419 1.21 0 2.176 1.096 2.157 2.42 0 1.333-.956 2.418-2.157 2.418zm7.975 0c-1.183 0-2.157-1.085-2.157-2.419 0-1.333.955-2.419 2.157-2.419 1.21 0 2.176 1.096 2.157 2.42 0 1.333-.946 2.418-2.157 2.418z"/>
            </svg>
          </div>
          <h3 class="text-xl font-semibold text-gray-900 dark:text-white mb-4">Discord</h3>
          <p class="text-gray-600 dark:text-gray-400 mb-6">加入我们的 Discord 社区</p>
          <a href="https://discord.com" target="_blank" rel="noopener" class="inline-flex items-center text-primary-500 hover:text-primary-600">
            <span>加入讨论</span>
            <svg class="w-4 h-4 ml-2" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M14 5l7 7m0 0l-7 7m7-7H3"/>
            </svg>
          </a>
        </div>

        <!-- 微信群 -->
        <div class="bg-gray-50 dark:bg-gray-800 rounded-xl p-8 text-center hover:shadow-lg transition-all duration-300">
          <div class="w-16 h-16 mx-auto bg-gradient-to-r from-primary-500 to-secondary-500 rounded-full flex items-center justify-center mb-6">
            <svg class="w-8 h-8 text-white" fill="currentColor" viewBox="0 0 24 24">
              <path d="M8.667 11.511c-.276 0-.5-.224-.5-.5s.224-.5.5-.5.5.224.5.5-.224.5-.5.5zm6.666 0c-.276 0-.5-.224-.5-.5s.224-.5.5-.5.5.224.5.5-.224.5-.5.5zm-8.666-7.5C3.198 4.011 1 6.631 1 9.777c0 1.964.941 3.728 2.404 4.866L2.11 17.988c-.093.349.219.636.548.506l2.96-1.183c.694.268 1.447.416 2.233.416 3.469 0 6.283-2.62 6.283-5.867 0-3.246-2.814-5.867-6.283-5.867zm13.666 12.178c1.464-1.138 2.404-2.902 2.404-4.866 0-3.146-2.198-5.766-4.667-5.766-3.469 0-6.283 2.62-6.283 5.867 0 3.246 2.814 5.867 6.283 5.867.786 0 1.539-.148 2.233-.416l2.96 1.183c.329.13.641-.157.548-.506l-1.294-3.345z"/>
            </svg>
          </div>
          <h3 class="text-xl font-semibold text-gray-900 dark:text-white mb-4">微信群</h3>
          <p class="text-gray-600 dark:text-gray-400 mb-6">扫码加入微信交流群</p>
          <button class="inline-flex items-center text-primary-500 hover:text-primary-600">
            <span>扫码加入</span>
            <svg class="w-4 h-4 ml-2" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M14 5l7 7m0 0l-7 7m7-7H3"/>
            </svg>
          </button>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { onMounted } from 'vue'
import gsap from 'gsap'
import ScrollTrigger from 'gsap/ScrollTrigger'

gsap.registerPlugin(ScrollTrigger)

onMounted(() => {
  // 卡片动画
  gsap.from('.grid > div', {
    scrollTrigger: {
      trigger: '.grid',
      start: 'top bottom-=100',
      toggleActions: 'play none none reverse'
    },
    y: 40,
    opacity: 0,
    duration: 1,
    stagger: 0.2,
    ease: 'power3.out'
  })
})
</script>

<style scoped>
.gradient-text {
  @apply bg-gradient-to-r from-primary-500 to-secondary-500 bg-clip-text text-transparent;
}
</style> 