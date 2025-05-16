<template>
  <div class="min-h-screen py-32 relative">
    <!-- 流星背景 -->
    <falling-stars-background
      color="255, 255, 255"
      :count="140"
      :speed="1.7"
      :trail-length="24"
      class="!fixed inset-0 -z-10"
    />
    
    <!-- 页面内容 -->
    <div class="container mx-auto px-4 sm:px-6 lg:px-8">
      <div class="text-center mb-16">
        <h1 class="text-4xl sm:text-5xl font-bold mb-4">
          <span class="text-transparent bg-clip-text bg-gradient-to-r from-blue-500 to-purple-500">
            解决方案
          </span>
        </h1>
        <p class="text-lg text-white/60 max-w-2xl mx-auto">
          我们为不同行业和场景提供专业的智能办公解决方案，助力企业数字化转型
        </p>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
        <div v-for="solution in solutions" :key="solution.title" 
          class="backdrop-blur-xl bg-white/5 border border-white/10 rounded-2xl p-6 hover:bg-white/10 transition-all duration-300 transform hover:scale-[1.02]">
          <div class="h-12 w-12 rounded-lg bg-gradient-to-br from-blue-500 to-purple-500 flex items-center justify-center mb-4">
            <component :is="solution.icon" class="h-6 w-6 text-white" />
          </div>
          <h3 class="text-xl font-semibold text-white mb-2">{{ solution.title }}</h3>
          <p class="text-white/60">{{ solution.description }}</p>
          <ul class="mt-4 space-y-2">
            <li v-for="feature in solution.features" :key="feature" 
              class="flex items-center text-white/60">
              <CheckIcon class="h-5 w-5 text-blue-400 mr-2" />
              {{ feature }}
            </li>
          </ul>
          <a href="#" 
            class="mt-6 inline-flex items-center text-blue-400 hover:text-blue-300 transition-colors">
            了解更多
            <ArrowRightIcon class="h-4 w-4 ml-1" />
          </a>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'
import { 
  ArrowRightIcon,
  CheckIcon,
  Cog6ToothIcon as CogIcon,
  UserGroupIcon as UsersIcon,
  ChartBarIcon,
  DevicePhoneMobileIcon,
  ChatBubbleBottomCenterTextIcon,
  ShieldCheckIcon
} from '@heroicons/vue/24/outline'
import FallingStarsBackground from '../components/FallingStarsBackground.vue'

const solutions = ref([
  {
    title: '智能工作流',
    description: '自动化业务流程，提高工作效率',
    icon: CogIcon,
    features: [
      '可视化流程设计',
      '智能任务分发',
      '自动化审批',
      '数据实时同步'
    ]
  },
  {
    title: '协同办公',
    description: '打破信息孤岛，实现无缝协作',
    icon: UsersIcon,
    features: [
      '实时文档协作',
      '团队即时沟通',
      '项目进度管理',
      '知识库共享'
    ]
  },
  {
    title: '数据分析',
    description: '深度挖掘数据价值，辅助决策',
    icon: ChartBarIcon,
    features: [
      '多维度数据分析',
      '自定义报表',
      '预测性分析',
      '数据可视化'
    ]
  },
  {
    title: '移动办公',
    description: '随时随地处理工作，提升效率',
    icon: DevicePhoneMobileIcon,
    features: [
      '移动端应用',
      '消息推送',
      '离线工作',
      '安全认证'
    ]
  },
  {
    title: '智能客服',
    description: '提供全天候智能客户服务',
    icon: ChatBubbleBottomCenterTextIcon,
    features: [
      'AI 对话机器人',
      '智能工单分配',
      '客户画像分析',
      '服务质量监控'
    ]
  },
  {
    title: '安全管理',
    description: '全方位保护企业数据安全',
    icon: ShieldCheckIcon,
    features: [
      '访问权限控制',
      '数据加密存储',
      '操作日志审计',
      '安全漏洞检测'
    ]
  }
])
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
</style> 