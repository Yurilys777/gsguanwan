<template>
  <footer class="bg-white dark:bg-gray-900 border-t border-gray-200 dark:border-gray-800">
    <div class="max-w-7xl mx-auto py-12 px-4 sm:px-6 lg:px-8">
      <div class="grid grid-cols-1 md:grid-cols-4 gap-8">
        <div>
          <a href="/" class="text-xl font-bold text-gray-900 dark:text-white">
            AutoSmartOA
          </a>
          <p class="mt-4 text-gray-600 dark:text-gray-400">
            自动化OA管理系统
          </p>
        </div>
        
        <div>
          <h3 class="text-sm font-semibold text-gray-900 dark:text-white uppercase tracking-wider">
            产品服务
          </h3>
          <ul class="mt-4 space-y-4">
            <li>
              <a href="/products/workflow" class="text-base text-gray-600 dark:text-gray-400 hover:text-gray-900 dark:hover:text-white">
                工作流管理
              </a>
            </li>
            <li>
              <a href="/products/document" class="text-base text-gray-600 dark:text-gray-400 hover:text-gray-900 dark:hover:text-white">
                文档协作
              </a>
            </li>
            <li>
              <a href="/products/hr" class="text-base text-gray-600 dark:text-gray-400 hover:text-gray-900 dark:hover:text-white">
                人事管理
              </a>
            </li>
          </ul>
        </div>

        <div>
          <h3 class="text-sm font-semibold text-gray-900 dark:text-white uppercase tracking-wider">
            解决方案
          </h3>
          <ul class="mt-4 space-y-4">
            <li>
              <a href="/solutions/enterprise" class="text-base text-gray-600 dark:text-gray-400 hover:text-gray-900 dark:hover:text-white">
                企业管理
              </a>
            </li>
            <li>
              <a href="/solutions/remote" class="text-base text-gray-600 dark:text-gray-400 hover:text-gray-900 dark:hover:text-white">
                远程办公
              </a>
            </li>
            <li>
              <a href="/solutions/digital" class="text-base text-gray-600 dark:text-gray-400 hover:text-gray-900 dark:hover:text-white">
                数字化转型
              </a>
            </li>
          </ul>
        </div>

        <div>
          <h3 class="text-sm font-semibold text-gray-900 dark:text-white uppercase tracking-wider">
            支持
          </h3>
          <ul class="mt-4 space-y-4">
            <li>
              <a href="/support/help" 
                 class="text-base text-gray-600 dark:text-gray-400 hover:text-gray-900 dark:hover:text-white">
                帮助中心
              </a>
            </li>
            <li>
              <a href="/support/contact" 
                 class="text-base text-gray-600 dark:text-gray-400 hover:text-gray-900 dark:hover:text-white">
                联系我们
              </a>
            </li>
            <li>
              <a href="/support/demo" 
                 class="text-base text-gray-600 dark:text-gray-400 hover:text-gray-900 dark:hover:text-white">
                预约演示
              </a>
            </li>
          </ul>
        </div>
      </div>
      
      <div class="mt-12 border-t border-gray-200 dark:border-gray-800 pt-8">
        <p class="text-base text-gray-500 dark:text-gray-400 text-center">
          &copy; {{ new Date().getFullYear() }} AutoSmartOA. 保留所有权利。
        </p>
      </div>
    </div>
  </footer>
</template>

<script setup>
// 页脚逻辑
</script> 