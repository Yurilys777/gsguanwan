<template>
  <div class="min-h-screen flex items-center justify-center py-32 px-4 sm:px-6 lg:px-8 relative">
    <!-- 粒子背景 -->
    <particles-background
      color="100, 116, 139"
      :particle-count="80"
      :connection-distance="150"
      :speed="0.3"
      class="!fixed inset-0 -z-10"
    />
    
    <!-- 登录表单 -->
    <div class="max-w-md w-full space-y-8 backdrop-blur-xl bg-white/5 p-8 rounded-2xl border border-white/10 shadow-xl">
      <div>
        <h2 class="mt-6 text-center text-3xl font-bold text-transparent bg-clip-text bg-gradient-to-r from-blue-400 to-purple-400">
          登录账户
        </h2>
        <p class="mt-2 text-center text-sm text-white/60">
          还没有账户？
          <router-link to="/register" class="font-medium text-blue-400 hover:text-blue-300 transition-colors">
            立即注册
          </router-link>
        </p>
      </div>
      <form class="mt-8 space-y-6" @submit.prevent="handleLogin">
        <div class="rounded-md space-y-4">
          <div>
            <label for="email" class="sr-only">邮箱地址</label>
            <input
              id="email"
              name="email"
              type="email"
              required
              class="appearance-none rounded-lg relative block w-full px-4 py-3 border border-white/10 bg-white/5 text-white placeholder-white/40 focus:outline-none focus:ring-2 focus:ring-blue-500 focus:border-transparent transition-colors"
              placeholder="邮箱地址"
              v-model="email"
            >
          </div>
          <div>
            <label for="password" class="sr-only">密码</label>
            <input
              id="password"
              name="password"
              type="password"
              required
              class="appearance-none rounded-lg relative block w-full px-4 py-3 border border-white/10 bg-white/5 text-white placeholder-white/40 focus:outline-none focus:ring-2 focus:ring-blue-500 focus:border-transparent transition-colors"
              placeholder="密码"
              v-model="password"
            >
          </div>
        </div>

        <div class="flex items-center justify-between">
          <div class="flex items-center">
            <input
              id="remember-me"
              name="remember-me"
              type="checkbox"
              class="h-4 w-4 bg-white/5 border-white/10 rounded text-blue-500 focus:ring-blue-500 transition-colors"
              v-model="rememberMe"
            >
            <label for="remember-me" class="ml-2 block text-sm text-white/60">
              记住我
            </label>
          </div>

          <div class="text-sm">
            <a href="#" class="font-medium text-blue-400 hover:text-blue-300 transition-colors">
              忘记密码？
            </a>
          </div>
        </div>

        <div>
          <button
            type="submit"
            class="group relative w-full flex justify-center py-3 px-4 border border-transparent rounded-lg text-sm font-medium text-white bg-gradient-to-r from-blue-500 to-purple-500 hover:from-blue-600 hover:to-purple-600 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-blue-500 transition-all duration-200 ease-in-out transform hover:scale-[1.02]"
          >
            登录
          </button>
        </div>
      </form>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'
import { useRouter } from 'vue-router'
import ParticlesBackground from '../components/ParticlesBackground.vue'

const router = useRouter()
const email = ref('')
const password = ref('')
const rememberMe = ref(false)

const handleLogin = async () => {
  try {
    // TODO: 实现登录逻辑
    console.log('登录信息：', {
      email: email.value,
      password: password.value,
      rememberMe: rememberMe.value
    })
    // 登录成功后跳转到首页
    router.push('/')
  } catch (error) {
    console.error('登录失败：', error)
  }
}
</script>

<style>
/* 优化滚动行为 */
html {
  scroll-behavior: smooth;
}

/* 确保内容在背景之上 */
.relative {
  isolation: isolate;
}

/* 输入框自动填充样式优化 */
input:-webkit-autofill,
input:-webkit-autofill:hover,
input:-webkit-autofill:focus {
  -webkit-text-fill-color: white;
  -webkit-box-shadow: 0 0 0px 1000px rgba(255, 255, 255, 0.05) inset;
  transition: background-color 5000s ease-in-out 0s;
}
</style> 