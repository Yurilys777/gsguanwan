<template>
  <canvas ref="canvas" class="fixed inset-0 w-full h-full"></canvas>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from 'vue'

const props = defineProps({
  color: {
    type: String,
    default: '255, 255, 255'
  },
  particleCount: {
    type: Number,
    default: 100
  },
  connectionDistance: {
    type: Number,
    default: 120
  },
  speed: {
    type: Number,
    default: 0.5
  }
})

const canvas = ref(null)
let ctx = null
let animationFrameId = null
let particles = []

class Particle {
  constructor() {
    this.reset()
  }

  reset() {
    this.x = Math.random() * window.innerWidth
    this.y = Math.random() * window.innerHeight
    this.vx = (Math.random() - 0.5) * props.speed
    this.vy = (Math.random() - 0.5) * props.speed
    this.radius = Math.random() * 2 + 1
  }

  update() {
    this.x += this.vx
    this.y += this.vy

    if (this.x < 0 || this.x > window.innerWidth) this.vx *= -1
    if (this.y < 0 || this.y > window.innerHeight) this.vy *= -1
  }

  draw() {
    ctx.beginPath()
    ctx.arc(this.x, this.y, this.radius, 0, Math.PI * 2)
    ctx.fillStyle = `rgba(${props.color}, 0.5)`
    ctx.fill()
    ctx.closePath()
  }
}

const drawConnections = () => {
  particles.forEach((particle, i) => {
    particles.slice(i + 1).forEach(otherParticle => {
      const dx = particle.x - otherParticle.x
      const dy = particle.y - otherParticle.y
      const distance = Math.sqrt(dx * dx + dy * dy)

      if (distance < props.connectionDistance) {
        const opacity = (1 - distance / props.connectionDistance) * 0.3
        ctx.beginPath()
        ctx.moveTo(particle.x, particle.y)
        ctx.lineTo(otherParticle.x, otherParticle.y)
        ctx.strokeStyle = `rgba(${props.color}, ${opacity})`
        ctx.stroke()
        ctx.closePath()
      }
    })
  })
}

const initParticles = () => {
  particles = Array(props.particleCount).fill().map(() => new Particle())
}

const resizeCanvas = () => {
  if (canvas.value) {
    canvas.value.width = window.innerWidth
    canvas.value.height = window.innerHeight
  }
}

const animate = () => {
  ctx.clearRect(0, 0, canvas.value.width, canvas.value.height)
  
  particles.forEach(particle => {
    particle.update()
    particle.draw()
  })
  
  drawConnections()
  
  animationFrameId = requestAnimationFrame(animate)
}

onMounted(() => {
  ctx = canvas.value.getContext('2d')
  resizeCanvas()
  initParticles()
  animate()
  
  window.addEventListener('resize', resizeCanvas)
})

onUnmounted(() => {
  if (animationFrameId) {
    cancelAnimationFrame(animationFrameId)
  }
  window.removeEventListener('resize', resizeCanvas)
})
</script> 