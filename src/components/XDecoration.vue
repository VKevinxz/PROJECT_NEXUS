<template>
  <div class="x-decoration-wrapper" :class="{ 'full-screen': fullScreen }">
    <!-- X principal estática -->
    <div class="x-decoration-container" :style="{ zIndex: zIndex }">
      <div class="x-line x-line-1" :style="{ backgroundColor: color, height: `${thickness}px` }"></div>
      <div class="x-line x-line-2" :style="{ backgroundColor: color, height: `${thickness}px` }"></div>
      <div v-if="showCircle" class="x-circle" :style="{ borderColor: color }">
        <slot name="circle-content">
          <!-- Contenido del círculo (puede ser una imagen o contenido personalizado) -->
        </slot>
      </div>
    </div>

    <!-- Múltiples Xs animadas (tipo watermark) -->
    <div v-if="multipleXs" class="animated-xs-container">
      <div 
        v-for="n in xsCount" 
        :key="n" 
        class="animated-x" 
        :style="{ 
          '--delay': `${n * 1.5}s`,
          '--duration': `${7 + Math.random() * 5}s`,
          '--scale': `${0.1 + Math.random() * 0.2}`,
          '--rotate': `${Math.random() * 360}deg`,
          '--top': `${Math.random() * 100}%`,
          '--left': `${Math.random() * 100}%`,
          '--opacity': `${0.1 + Math.random() * 0.2}`
        }"
      >
        <div 
          class="animated-x-line watermark-line" 
          :style="{ 
            backgroundColor: animationColors[n % animationColors.length], 
            height: `${Math.max(1, thickness * 0.2)}px`,
            opacity: 'var(--opacity)'
          }"
        ></div>
        <div 
          class="animated-x-line watermark-line" 
          :style="{ 
            backgroundColor: animationColors[n % animationColors.length], 
            height: `${Math.max(1, thickness * 0.2)}px`,
            opacity: 'var(--opacity)'
          }"
        ></div>
      </div>
    </div>

    <!-- Elementos de partículas flotantes para mayor efecto -->
    <div v-if="showParticles" class="particles-container">
      <!-- Partículas del lado izquierdo -->
      <div 
        v-for="n in particlesCount" 
        :key="`p-left-${n}`" 
        class="particle particle-left"
        :style="{ 
          '--p-delay': `${n * 0.5 + Math.random() * 2}s`,
          '--p-duration': `${3 + Math.random() * 4}s`,
          '--p-size': `${3 + Math.random() * 8}px`,
          '--p-color': animationColors[Math.floor(Math.random() * animationColors.length)],
          '--p-top': `${Math.random() * 100}%`,
          '--p-start': `${Math.random() * 10}%`,
          '--p-end': `${30 + Math.random() * 20}%`,
        }"
      ></div>
      
      <!-- Partículas del lado derecho -->
      <div 
        v-for="n in particlesCount" 
        :key="`p-right-${n}`" 
        class="particle particle-right"
        :style="{ 
          '--p-delay': `${n * 0.5 + Math.random() * 2}s`,
          '--p-duration': `${3 + Math.random() * 4}s`,
          '--p-size': `${3 + Math.random() * 8}px`,
          '--p-color': animationColors[Math.floor(Math.random() * animationColors.length)],
          '--p-top': `${Math.random() * 100}%`,
          '--p-start': `${90 + Math.random() * 10}%`,
          '--p-end': `${50 + Math.random() * 20}%`,
        }"
      ></div>
      
      <!-- Partículas de Xs pequeñas como watermark -->
      <div 
        v-for="n in particlesCount" 
        :key="`p-x-${n}`" 
        class="particle-x"
        :style="{ 
          '--x-delay': `${n * 0.7 + Math.random() * 3}s`,
          '--x-duration': `${5 + Math.random() * 5}s`,
          '--x-size': `${6 + Math.random() * 10}px`,
          '--x-color': animationColors[Math.floor(Math.random() * animationColors.length)],
          '--x-top': `${Math.random() * 100}%`,
          '--x-left': `${Math.random() * 100}%`,
          '--x-opacity': `${0.1 + Math.random() * 0.15}`,
        }"
      >
        <div class="particle-x-line" :style="{ backgroundColor: 'var(--x-color)', height: '1px' }"></div>
        <div class="particle-x-line" :style="{ backgroundColor: 'var(--x-color)', height: '1px' }"></div>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'XDecoration',
  props: {
    color: {
      type: String,
      default: '#FFAE14' // Color naranja por defecto
    },
    thickness: {
      type: Number,
      default: 100 // Grosor de las líneas en píxeles (aumentado)
    },
    showCircle: {
      type: Boolean,
      default: false
    },
    fullScreen: {
      type: Boolean,
      default: false
    },
    zIndex: {
      type: Number,
      default: 0
    },
    multipleXs: {
      type: Boolean,
      default: false
    },
    xsCount: {
      type: Number,
      default: 5
    },
    showParticles: {
      type: Boolean,
      default: false
    },
    particlesCount: {
      type: Number,
      default: 15
    }
  },
  data() {
    return {
      animationColors: ['#FFAE14', '#E7683A', '#E86934', '#ffd166', '#ff9e00']
    }
  }
})
</script>

<style scoped>
.x-decoration-wrapper {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  overflow: hidden;
  pointer-events: none;
}

.x-decoration-wrapper.full-screen {
  position: fixed;
  z-index: 0;
}

.x-decoration-container {
  position: relative;
  width: 100%;
  height: 100%;
}

.x-line {
  position: absolute;
  top: 60%;
  right: -30%;
  width: 160%;
  transform-origin: center;
  box-shadow: 0 0 20px rgba(255, 174, 20, 0.6);
}

.x-line-1 {
  transform: rotate(45deg) translateY(-50%);
}

.x-line-2 {
  transform: rotate(-45deg) translateY(-50%);
}

.x-circle {
  position: absolute;
  width: 150px;
  height: 150px;
  border-radius: 50%;
  background-color: white;
  border: 5px solid;
  top: calc(50% - 75px);
  left: calc(50% - 75px);
  overflow: hidden;
  display: flex;
  align-items: center;
  justify-content: center;
  box-shadow: 0 4px 15px rgba(0, 0, 0, 0.15);
  z-index: 1;
}

/* Estilos para las Xs animadas */
.animated-xs-container {
  position: absolute;
  width: 100%;
  height: 100%;
  top: 0;
  left: 0;
  z-index: 0;
}

.animated-x {
  position: absolute;
  width: 80px;
  height: 80px;
  opacity: 0;
  top: var(--top, 50%);
  left: var(--left, 50%);
  transform: scale(var(--scale, 0.3)) rotate(var(--rotate, 0deg));
  animation: floatX var(--duration, 8s) ease-in-out infinite var(--delay, 0s);
}

.animated-x-line {
  position: absolute;
  top: 50%;
  left: 0;
  width: 100%;
  height: 12px;
  transform-origin: center;
  box-shadow: 0 0 8px rgba(255, 174, 20, 0.2);
}

.animated-x-line.watermark-line {
  box-shadow: 0 0 5px rgba(255, 174, 20, 0.1);
}

.animated-x-line:first-child {
  transform: rotate(45deg) translateY(-50%);
}

.animated-x-line:last-child {
  transform: rotate(-45deg) translateY(-50%);
}

/* Partículas flotantes */
.particles-container {
  position: absolute;
  width: 100%;
  height: 100%;
  top: 0;
  left: 0;
}

.particle {
  position: absolute;
  width: var(--p-size, 8px);
  height: var(--p-size, 8px);
  background-color: var(--p-color, #FFAE14);
  border-radius: 50%;
  opacity: 0;
  filter: blur(1px);
  box-shadow: 0 0 8px var(--p-color, #FFAE14);
  top: var(--p-top, 50%);
}

/* Partícula desde la izquierda hacia el centro */
.particle-left {
  left: var(--p-start, 0%);
  animation: moveFromLeft var(--p-duration, 4s) ease-in-out infinite var(--p-delay, 0s);
}

/* Partícula desde la derecha hacia el centro */
.particle-right {
  right: calc(100% - var(--p-start, 100%));
  animation: moveFromRight var(--p-duration, 4s) ease-in-out infinite var(--p-delay, 0s);
}

/* Partículas de X tipo watermark */
.particle-x {
  position: absolute;
  width: var(--x-size, 8px);
  height: var(--x-size, 8px);
  top: var(--x-top, 50%);
  left: var(--x-left, 50%);
  opacity: 0;
  animation: floatParticleX var(--x-duration, 6s) ease-in-out infinite var(--x-delay, 0s);
}

.particle-x-line {
  position: absolute;
  top: 50%;
  left: 0;
  width: 100%;
  height: 1px;
  transform-origin: center;
  opacity: var(--x-opacity, 0.1);
}

.particle-x-line:first-child {
  transform: rotate(45deg) translateY(-50%);
}

.particle-x-line:last-child {
  transform: rotate(-45deg) translateY(-50%);
}

@keyframes floatX {
  0% {
    transform: scale(var(--scale)) rotate(var(--rotate));
    opacity: 0;
  }
  25% {
    opacity: var(--opacity, 0.4);
  }
  50% {
    transform: scale(var(--scale)) translate(50px, -50px) rotate(calc(var(--rotate) + 15deg));
    opacity: var(--opacity, 0.6);
  }
  75% {
    opacity: var(--opacity, 0.3);
  }
  100% {
    transform: scale(var(--scale)) translate(0, 0) rotate(var(--rotate));
    opacity: 0;
  }
}

@keyframes moveFromLeft {
  0% {
    left: var(--p-start, 0%);
    opacity: 0;
  }
  20% {
    opacity: 0.8;
  }
  70% {
    opacity: 0.4;
  }
  100% {
    left: var(--p-end, 50%);
    opacity: 0;
  }
}

@keyframes moveFromRight {
  0% {
    right: calc(100% - var(--p-start, 100%));
    opacity: 0;
  }
  20% {
    opacity: 0.8;
  }
  70% {
    opacity: 0.4;
  }
  100% {
    right: calc(100% - var(--p-end, 50%));
    opacity: 0;
  }
}

@keyframes floatParticleX {
  0% {
    transform: translate(0, 0) rotate(0deg);
    opacity: 0;
  }
  25% {
    opacity: var(--x-opacity, 0.15);
  }
  50% {
    transform: translate(30px, -20px) rotate(10deg);
    opacity: var(--x-opacity, 0.15);
  }
  75% {
    opacity: var(--x-opacity, 0.1);
  }
  100% {
    transform: translate(0, 0) rotate(0deg);
    opacity: 0;
  }
}

@media (max-width: 768px) {
  .x-line {
    width: 250%;
    right: -70%;
  }
  
  .x-circle {
    width: 100px;
    height: 100px;
    top: calc(50% - 50px);
    left: calc(50% - 50px);
  }
  
  .animated-x {
    width: 50px;
    height: 50px;
  }
}
</style>