<template>
  <footer class="bg-gray-900/95 backdrop-blur-md border-t border-gray-800 shadow-lg">
    <div class="max-w-7xl mx-auto py-12 px-4 sm:px-6 lg:px-8">
      <div class="grid grid-cols-2 md:grid-cols-4 gap-8">
        <div>
          <h3 class="text-lg font-semibold text-white mb-4">关于我们</h3>
          <ul class="space-y-2">
            <li><router-link to="/about" class="text-gray-300 hover:text-white transition-colors">公司简介</router-link></li>
            <li><router-link to="/about" class="text-gray-300 hover:text-white transition-colors">发展历程</router-link></li>
            <li><router-link to="/about" class="text-gray-300 hover:text-white transition-colors">企业文化</router-link></li>
            <li><router-link to="/about" class="text-gray-300 hover:text-white transition-colors">加入我们</router-link></li>
          </ul>
        </div>
        <div>
          <h3 class="text-lg font-semibold text-white mb-4">产品服务</h3>
          <ul class="space-y-2">
            <li><router-link to="/products" class="text-gray-300 hover:text-white transition-colors">OA系统</router-link></li>
            <li><router-link to="/services" class="text-gray-300 hover:text-white transition-colors">协同办公</router-link></li>
            <li><router-link to="/services" class="text-gray-300 hover:text-white transition-colors">流程管理</router-link></li>
            <li><router-link to="/services" class="text-gray-300 hover:text-white transition-colors">文档管理</router-link></li>
          </ul>
        </div>
        <div>
          <h3 class="text-lg font-semibold text-white mb-4">解决方案</h3>
          <ul class="space-y-2">
            <li><router-link to="/solutions" class="text-gray-300 hover:text-white transition-colors">中小企业方案</router-link></li>
            <li><router-link to="/solutions" class="text-gray-300 hover:text-white transition-colors">大型企业方案</router-link></li>
            <li><router-link to="/solutions" class="text-gray-300 hover:text-white transition-colors">定制化开发</router-link></li>
            <li><router-link to="/solutions" class="text-gray-300 hover:text-white transition-colors">行业解决方案</router-link></li>
          </ul>
        </div>
        <div>
          <h3 class="text-lg font-semibold text-white mb-4">联系我们</h3>
          <ul class="space-y-2">
            <li class="text-gray-300">电话：400-999-8794</li>
            <li class="text-gray-300">邮箱：contact@autosmartoa.com</li>
            <li class="text-gray-300">地址：东莞市周屋基村小雅立创大厦1号楼402</li>
            <li class="text-gray-300">工作时间：周一至周五 9:00-18:00</li>
          </ul>
        </div>
      </div>
      <div class="mt-8 pt-8 border-t border-gray-800">
        <p class="text-center text-gray-300">
          © {{ new Date().getFullYear() }} AutoSmartOA. 版权所有 粤ICP备2024334466号
        </p>
      </div>
    </div>
  </footer>
</template>

<script setup>
</script>

<style scoped>
</style> 