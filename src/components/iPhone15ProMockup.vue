<template>
  <div class="iphone-mockup-container">
    <svg :width="width" :height="height" viewBox="0 0 433 882" fill="none" xmlns="http://www.w3.org/2000/svg">
      <!-- 手机外壳 -->
      <g>
        <rect x="16.5" y="16.5" width="400" height="849" rx="63.5" class="iphone-frame" />
        <rect x="14" y="14" width="405" height="854" rx="66" stroke-width="5" class="iphone-border" />
        
        <!-- 动态岛 -->
        <rect x="161" y="36" width="111" height="29" rx="14.5" fill="#000000" />
        
        <!-- 按钮 -->
        <rect x="0" y="196" width="5" height="60" rx="2.5" class="button" />
        <rect x="0" y="276" width="5" height="120" rx="2.5" class="button" />
        <rect x="428" y="227" width="5" height="100" rx="2.5" class="button" />
        
        <!-- 屏幕区域 - 用于显示图片 -->
        <foreignObject x="22" y="75" width="390" height="730">
          <div xmlns="http://www.w3.org/1999/xhtml" class="screen">
            <img v-if="src" :src="src" alt="App Screenshot" class="screen-image" />
            <div v-else class="empty-screen">
              <slot>
                <div class="placeholder-text">应用界面</div>
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
  width: {
    type: Number,
    default: 433
  },
  height: {
    type: Number,
    default: 882
  },
  src: {
    type: String,
    default: null
  }
})
</script>

<style scoped>
.iphone-mockup-container {
  display: inline-block;
  position: relative;
}

.iphone-frame {
  fill: #1E1E1E;
  stroke: rgba(255, 255, 255, 0.12);
  stroke-width: 1px;
}

.iphone-border {
  stroke: #2A2A2A;
  stroke-opacity: 0.8;
}

.button {
  fill: #2A2A2A;
}

.screen {
  width: 100%;
  height: 100%;
  background-color: #121212;
  border-radius: 4px;
  overflow: hidden;
  display: flex;
  align-items: center;
  justify-content: center;
}

.screen-image {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.empty-screen {
  width: 100%;
  height: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  color: rgba(255, 255, 255, 0.5);
}

.placeholder-text {
  font-size: 14px;
  text-align: center;
}

@media (prefers-color-scheme: light) {
  .iphone-frame {
    fill: #F2F2F2;
    stroke: rgba(0, 0, 0, 0.12);
  }
  
  .iphone-border {
    stroke: #D1D1D1;
  }
  
  .button {
    fill: #D1D1D1;
  }
  
  .screen {
    background-color: #FFFFFF;
  }
  
  .empty-screen {
    color: rgba(0, 0, 0, 0.5);
  }
}
</style> 