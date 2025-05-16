<template>
  <section class="py-24 relative overflow-hidden">
    <!-- 背景装饰 -->
    <div class="absolute inset-0 bg-gradient-to-b from-blue-500/5 to-purple-500/5"></div>
    
    <!-- 标题区域 -->
    <div class="container mx-auto px-4 sm:px-6 lg:px-8">
      <div class="text-center mb-16">
        <h2 class="text-4xl md:text-5xl font-bold">
          <span class="text-transparent bg-clip-text bg-gradient-to-r from-[#4F94FF] to-[#8C65FD]">作品</span>
        </h2>
        <p class="mt-4 text-base text-white/60">
          我们的优秀案例
        </p>
      </div>

      <!-- 作品网格 -->
      <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
        <template v-for="(project, index) in projects" :key="index">
          <div 
            class="portfolio-item group relative overflow-hidden rounded-2xl bg-gray-900/50 backdrop-blur-sm border border-white/10 p-8 hover:bg-gray-900/70 transition-all duration-300"
          >
            <!-- 项目图标 -->
            <div class="w-14 h-14 mb-6 rounded-xl flex items-center justify-center" :class="project.iconBg">
              <component :is="project.icon" class="w-7 h-7" :class="project.iconColor" />
            </div>
            
            <!-- 项目信息 -->
            <h3 class="text-2xl font-bold text-white mb-3">{{ project.title }}</h3>
            <p class="text-white/60 text-base leading-relaxed">{{ project.description }}</p>
          </div>
        </template>
      </div>
    </div>
  </section>
</template>

<script setup>
import { 
  UserGroupIcon, 
  ChartBarIcon,
  DevicePhoneMobileIcon,
  CloudIcon,
  ShieldCheckIcon,
  CogIcon
} from '@heroicons/vue/24/outline'

const projects = [
  {
    title: '社交应用',
    description: '连接用户的互动平台',
    icon: UserGroupIcon,
    iconBg: 'bg-emerald-500/20',
    iconColor: 'text-emerald-400'
  },
  {
    title: '数据可视化',
    description: '直观的数据分析展示',
    icon: ChartBarIcon,
    iconBg: 'bg-blue-500/20',
    iconColor: 'text-blue-400'
  },
  {
    title: '移动应用',
    description: '跨平台移动解决方案',
    icon: DevicePhoneMobileIcon,
    iconBg: 'bg-purple-500/20',
    iconColor: 'text-purple-400'
  },
  {
    title: '云服务',
    description: '安全可靠的云端部署',
    icon: CloudIcon,
    iconBg: 'bg-sky-500/20',
    iconColor: 'text-sky-400'
  },
  {
    title: '安全防护',
    description: '全方位的数据安全保障',
    icon: ShieldCheckIcon,
    iconBg: 'bg-red-500/20',
    iconColor: 'text-red-400'
  },
  {
    title: '自动化流程',
    description: '智能工作流程管理',
    icon: CogIcon,
    iconBg: 'bg-amber-500/20',
    iconColor: 'text-amber-400'
  }
]
</script>

<style scoped>
.portfolio-item {
  transform: translateY(0);
  transition: all 0.3s ease-in-out;
}

.portfolio-item:hover {
  transform: translateY(-5px);
}
</style> 