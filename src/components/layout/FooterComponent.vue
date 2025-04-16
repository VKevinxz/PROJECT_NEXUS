<template>
  <footer class="bg-[#393D46] text-white py-8 transition-all duration-300 ease-in-out">
    <div class="container mx-auto px-4">
      <div class="flex flex-col md:flex-row justify-between items-center">
        <div class="mb-4 md:mb-0 transform hover:scale-105 transition-transform duration-300">
          <p>&copy; {{ currentYear }} NEXOS Estrategias & Negocios. Todos los derechos reservados.</p>
        </div>

        <div class="flex items-center transform hover:scale-105 transition-transform duration-300">
          <img src="@/assets/logo.svg" alt="Logo" class="h-8 mr-2 invert" />
          <div class="text-sm">
            <p>Una firma de expertos</p>
            <p>Sirviendo desde 2025</p>
          </div>
        </div>
      </div>
    </div>
  </footer>
</template>

<script lang="ts">
import { defineComponent, computed } from 'vue'

export default defineComponent({
  name: 'FooterComponent',
  setup() {
    const currentYear = computed(() => new Date().getFullYear())
    
    return {
      currentYear
    }
  }
})
</script>