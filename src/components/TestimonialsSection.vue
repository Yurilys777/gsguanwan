<template>
  <section class="py-24 relative overflow-hidden">
    <!-- 背景装饰 -->
    <div class="absolute inset-0 bg-gradient-radial from-blue-500/5 via-purple-500/5 to-transparent"></div>
    
    <!-- 标题 -->
    <div class="container mx-auto px-4 sm:px-6 lg:px-8">
      <h2 class="text-4xl md:text-5xl font-bold text-center mb-4">
        <span class="text-transparent bg-clip-text bg-gradient-to-r from-blue-400 via-purple-400 to-pink-400">
          用户声音
        </span>
      </h2>
      <p class="text-gray-400 text-center mb-12">来自我们用户的真实反馈</p>

      <!-- 评价卡片网格 -->
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8 relative testimonials-container px-8">
        <template v-for="(testimonial, index) in testimonials" :key="index">
          <div class="group relative backdrop-blur-xl bg-gray-900/50 border border-white/10 rounded-2xl p-8 transition-all duration-300 hover:bg-gray-900/70 mb-16 transform hover:scale-[1.02] hover:-translate-y-1"
               :style="{ transform: `translateY(${index % 3 * 40}px)` }">
            <!-- 装饰性引号 -->
            <div class="absolute -top-8 -left-6 text-8xl text-purple-500/20 font-serif leading-none opacity-60 group-hover:opacity-100 transition-opacity">"</div>
            
            <!-- 用户头像和信息 -->
            <div class="flex items-center mb-6 relative z-10">
              <div class="w-12 h-12 rounded-full bg-gray-800 flex items-center justify-center group-hover:bg-gray-700 transition-colors">
                <svg class="w-6 h-6 text-gray-600 group-hover:text-gray-400 transition-colors" fill="currentColor" viewBox="0 0 20 20">
                  <path fill-rule="evenodd" d="M10 9a3 3 0 100-6 3 3 0 000 6zm-7 9a7 7 0 1114 0H3z" clip-rule="evenodd" />
                </svg>
              </div>
              <div class="ml-4">
                <h3 class="text-lg font-medium text-white">{{ testimonial.name }}</h3>
                <p class="text-sm text-white/40 group-hover:text-white/60 transition-colors">{{ testimonial.title }}</p>
              </div>
            </div>
            
            <!-- 评价内容 -->
            <p class="text-base text-white/60 leading-relaxed relative z-10 mb-4 group-hover:text-white/80 transition-colors">{{ testimonial.content }}</p>
            
            <!-- 装饰性结束引号 -->
            <div class="absolute -bottom-16 -right-6 text-8xl text-purple-500/20 font-serif rotate-180 leading-none opacity-60 group-hover:opacity-100 transition-opacity">"</div>
          </div>
        </template>
      </div>
    </div>
  </section>
</template>

<script setup>
const testimonials = [
  {
    name: 'Lisa Wang',
    title: '制造业企业主管',
    content: '我们公司导入AutoSmartOA后，工作流程变得更加清晰高效。特别是审批流程的自动化处理，极大地提高了我们的运营效率。系统的智能分析功能也帮助我们更好地进行决策。'
  },
  {
    name: 'Michael Chen',
    title: '人力资源总监',
    content: '作为HR，AutoSmartOA的人事管理模块给我们带来了极大便利。从员工入职、培训到绩效考核，所有流程都实现了数字化管理，数据的整合分析也让人力资源工作变得更加科学。'
  },
  {
    name: 'Emma Zhang',
    title: 'IT部门主管',
    content: '系统的技术架构非常先进，集成了AI技术，既保证了稳定性又具备了很强的扩展性。最重要的是，它的安全性和权限管理非常完善，完全符合企业级应用的要求。'
  },
  {
    name: 'David Liu',
    title: '财务部门经理',
    content: '财务模块的自动化程度很高，从报销单据识别到凭证生成，都可以自动完成。系统还能智能提醒付款时间，帮助我们更好地管理现金流。'
  },
  {
    name: 'Sarah Li',
    title: '行政部门主管',
    content: '日常行政工作通过AutoSmartOA变得井井有条，无论是会议室预订、物资采购还是文件管理，都可以在系统中轻松完成。员工们也都反映系统非常容易上手。'
  },
  {
    name: 'Kevin Wu',
    title: '中小企业CEO',
    content: '作为一家成长期的企业，AutoSmartOA帮助我们实现了管理的规范化和自动化，性价比很高。它的模块化设计让我们可以根据需求逐步扩展功能，非常适合企业成长。'
  }
]
</script>

<style scoped>
.testimonials-container {
  perspective: 1000px;
  padding-bottom: 4rem;
}
</style> 