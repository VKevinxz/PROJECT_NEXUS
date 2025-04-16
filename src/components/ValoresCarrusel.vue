<template>
  <div class="py-16 bg-[#E9E9E9]">
    <div class="container mx-auto px-4">
      <h2 class="text-3xl font-bold text-center mb-12 text-[#393D46] animate-fade-in">Valores Corporativos</h2>

      <!-- Valores Carrusel -->
      <div class="relative max-w-5xl mx-auto overflow-hidden">
        <!-- Controles de navegación -->
        <div class="absolute top-1/2 left-0 transform -translate-y-1/2 z-10">
          <button 
            @click="prevSlide" 
            class="bg-white rounded-full p-2 shadow-md text-[#FFAE14] hover:text-[#E7683A] transition-all duration-300 hover:scale-110 focus:outline-none"
            aria-label="Anterior valor"
          >
            <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 19l-7-7 7-7" />
            </svg>
          </button>
        </div>
        
        <div class="absolute top-1/2 right-0 transform -translate-y-1/2 z-10">
          <button 
            @click="nextSlide" 
            class="bg-white rounded-full p-2 shadow-md text-[#FFAE14] hover:text-[#E7683A] transition-all duration-300 hover:scale-110 focus:outline-none"
            aria-label="Siguiente valor"
          >
            <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7" />
            </svg>
          </button>
        </div>

        <!-- Carrusel -->
        <div class="flex transition-transform duration-500 ease-in-out" :style="{ transform: `translateX(-${currentSlide * 100}%)` }">
          <div v-for="(valor, index) in valores" :key="index" class="w-full flex-shrink-0 px-4">
            <div class="bg-white p-8 rounded-lg shadow-md flex flex-col transform transition-all duration-500" 
                 :class="{'scale-105': currentSlide === index}">
              <div class="text-[#FFAE14] mb-3 text-5xl font-serif">"</div>
              <p class="text-[#393D46] mb-4 italic text-lg">
                {{ valor.quote }}
              </p>
              <div class="mt-auto text-[#E7683A] font-semibold">{{ valor.author }}</div>
            </div>
          </div>
        </div>

        <!-- Indicadores de paginación -->
        <div class="flex justify-center mt-6 space-x-2">
          <button 
            v-for="(_, index) in valores" 
            :key="index"
            @click="goToSlide(index)"
            :class="[
              'w-2.5 h-2.5 rounded-full transition-all duration-300',
              currentSlide === index ? 'bg-[#FFAE14] w-6' : 'bg-[#E7683A] opacity-50 hover:opacity-75'
            ]"
            :aria-label="`Ir al valor ${index + 1}`"
          ></button>
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent, ref, onMounted } from 'vue'

export default defineComponent({
  name: 'ValoresCarrusel',
  setup() {
    const currentSlide = ref(0)
    const autoplayInterval = ref<number | null>(null)
    
    const valores = [
      {
        quote: 'La disciplina es el puente entre las metas y el logro',
        author: '- Jim Rohn'
      },
      {
        quote: 'La integridad es hacer lo correcto aunque nadie esté mirando',
        author: '- Jim Stovall'
      },
      {
        quote: 'La innovación constante es la única forma de mantenerse competitivo a largo plazo',
        author: '- Jorge Gonzales'
      },
      {
        quote: 'La confidencialidad es una virtud de la lealtad, la lealtad es la virtud de la fidelidad',
        author: '- Edwin Louis'
      }
    ]
    
    const nextSlide = () => {
      currentSlide.value = (currentSlide.value + 1) % valores.length
      resetAutoplay()
    }
    
    const prevSlide = () => {
      currentSlide.value = (currentSlide.value - 1 + valores.length) % valores.length
      resetAutoplay()
    }
    
    const goToSlide = (index: number) => {
      currentSlide.value = index
      resetAutoplay()
    }
    
    const startAutoplay = () => {
      autoplayInterval.value = window.setInterval(() => {
        nextSlide()
      }, 5000) as unknown as number
    }
    
    const resetAutoplay = () => {
      if (autoplayInterval.value !== null) {
        clearInterval(autoplayInterval.value)
        startAutoplay()
      }
    }
    
    onMounted(() => {
      startAutoplay()
    })
    
    return {
      currentSlide,
      valores,
      nextSlide,
      prevSlide,
      goToSlide
    }
  }
})
</script>

<style scoped>
.animate-fade-in {
  animation: fadeIn 1s ease-in-out;
}

@keyframes fadeIn {
  from { opacity: 0; transform: translateY(20px); }
  to { opacity: 1; transform: translateY(0); }
}
</style>