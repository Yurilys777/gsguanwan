<template>
  <div class="absolute inset-0 -z-10 overflow-hidden">
    <div class="grid-container">
      <div v-for="i in totalBeams" :key="i" class="beam" :style="getBeamStyle(i)"></div>
    </div>
  </div>
</template>

<script setup>
import { computed } from 'vue'

const props = defineProps({
  perspective: {
    type: Number,
    default: 100
  },
  beamsPerSide: {
    type: Number,
    default: 3
  },
  beamSize: {
    type: Number,
    default: 5
  },
  beamDelayMax: {
    type: Number,
    default: 3
  },
  beamDelayMin: {
    type: Number,
    default: 0
  },
  beamDuration: {
    type: Number,
    default: 3
  },
  gridColor: {
    type: String,
    default: 'rgba(99, 102, 241, 0.15)'
  }
})

const totalBeams = computed(() => props.beamsPerSide * 4)

const getBeamStyle = (index) => {
  const side = Math.floor((index - 1) / props.beamsPerSide)
  const position = ((index - 1) % props.beamsPerSide + 1) / (props.beamsPerSide + 1)
  const delay = props.beamDelayMin + Math.random() * (props.beamDelayMax - props.beamDelayMin)
  
  let style = {
    '--beam-size': `${props.beamSize}px`,
    '--beam-duration': `${props.beamDuration}s`,
    '--beam-delay': `${delay}s`,
    '--beam-perspective': `${props.perspective}px`,
    '--beam-color': props.gridColor,
    animationDelay: `${delay}s`,
    animationDuration: `${props.beamDuration}s`
  }

  switch (side) {
    case 0: // top
      style = {
        ...style,
        left: `${position * 100}%`,
        top: '0'
      }
      break
    case 1: // right
      style = {
        ...style,
        right: '0',
        top: `${position * 100}%`
      }
      break
    case 2: // bottom
      style = {
        ...style,
        right: `${position * 100}%`,
        bottom: '0'
      }
      break
    case 3: // left
      style = {
        ...style,
        left: '0',
        bottom: `${position * 100}%`
      }
      break
  }

  return style
}
</script>

<style scoped>
.grid-container {
  position: absolute;
  inset: -100px;
  perspective: var(--beam-perspective);
  perspective-origin: center;
  transform-style: preserve-3d;
}

.beam {
  position: absolute;
  width: var(--beam-size);
  height: var(--beam-size);
  background: var(--beam-color);
  border-radius: 50%;
  animation: beam-animation var(--beam-duration) ease-in-out infinite;
}

@keyframes beam-animation {
  0% {
    transform: translateZ(0) scale(1);
    opacity: 0;
  }
  50% {
    transform: translateZ(200px) scale(2);
    opacity: 1;
  }
  100% {
    transform: translateZ(0) scale(1);
    opacity: 0;
  }
}
</style> 