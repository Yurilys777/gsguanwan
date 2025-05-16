<template>
  <div class="safari-mockup-container">
    <svg :width="width" :height="height" viewBox="0 0 1203 753" fill="none" xmlns="http://www.w3.org/2000/svg">
      <!-- Safari浏览器框架 -->
      <g>
        <!-- 浏览器外框 -->
        <rect x="0" y="0" width="1203" height="753" rx="8" class="window-frame" />
        
        <!-- 浏览器标题栏 -->
        <rect x="0" y="0" width="1203" height="38" rx="8 8 0 0" class="title-bar" />
        
        <!-- 关闭/最小化/最大化按钮 -->
        <circle cx="20" cy="19" r="6" fill="#FF5F57" />
        <circle cx="42" cy="19" r="6" fill="#FEBC2E" />
        <circle cx="64" cy="19" r="6" fill="#28C840" />
        
        <!-- 地址栏 -->
        <rect x="128" y="10" width="947" height="25" rx="4" class="address-bar" />
        <text x="148" y="26" class="url-text">{{ url || 'https://autosmartoa.com/dashboard' }}</text>
        
        <!-- 内容区域 -->
        <rect x="0" y="40" width="1203" height="713" rx="0 0 8 8" class="content-area" />
        
        <!-- 显示图片 -->
        <foreignObject x="0" y="40" width="1203" height="713">
          <div xmlns="http://www.w3.org/1999/xhtml" class="browser-content">
            <img v-if="src" :src="src" alt="Website Screenshot" class="content-image" />
            <div v-else class="empty-content">
              <slot>
                <div class="placeholder-content">
                  <div class="placeholder-logo">AutoSmartOA</div>
                  <div class="placeholder-text">智能办公系统界面</div>
                </div>
              </slot>
            </div>
          </div>
        </foreignObject>
      </g>
    </svg>
  </div>
</template>

<script setup>
defineProps({
  url: {
    type: String,
    default: null
  },
  src: {
    type: String,
    default: null
  },
  width: {
    type: Number,
    default: 1203
  },
  height: {
    type: Number,
    default: 753
  }
})
</script>

<style scoped>
.safari-mockup-container {
  display: inline-block;
  position: relative;
}

.window-frame {
  fill: #F2F2F7;
  stroke: #E0E0E5;
  stroke-width: 1px;
}

.title-bar {
  fill: #F2F2F7;
  stroke: #E0E0E5;
  stroke-width: 1px;
}

.address-bar {
  fill: #E9E9EB;
  stroke: #D8D8DC;
  stroke-width: 0.5px;
}

.url-text {
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
  font-size: 12px;
  fill: #4B4B4B;
}

.content-area {
  fill: #FFFFFF;
}

.browser-content {
  width: 100%;
  height: 100%;
  background-color: #FFFFFF;
  overflow: hidden;
}

.content-image {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.empty-content {
  width: 100%;
  height: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  background-color: #FFFFFF;
}

.placeholder-content {
  text-align: center;
}

.placeholder-logo {
  font-size: 32px;
  font-weight: bold;
  background: linear-gradient(90deg, #3B82F6, #8B5CF6);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  margin-bottom: 16px;
}

.placeholder-text {
  font-size: 18px;
  color: #71717A;
}

/* 深色模式 */
@media (prefers-color-scheme: dark) {
  .window-frame {
    fill: #1E1E1E;
    stroke: #333333;
  }
  
  .title-bar {
    fill: #2D2D2D;
    stroke: #333333;
  }
  
  .address-bar {
    fill: #3A3A3C;
    stroke: #444444;
  }
  
  .url-text {
    fill: #EEEEEE;
  }
  
  .content-area {
    fill: #2D2D2D;
  }
  
  .browser-content {
    background-color: #2D2D2D;
  }
  
  .empty-content {
    background-color: #2D2D2D;
  }
  
  .placeholder-text {
    color: #A1A1AA;
  }
}
</style> 