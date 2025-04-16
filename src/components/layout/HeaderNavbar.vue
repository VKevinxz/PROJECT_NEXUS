<template>
  <header 
    class="fixed w-full z-50 transition-all duration-300 ease-in-out"
    :class="[
      scrolled 
        ? 'bg-[#393D46]/95 backdrop-blur-md py-2 shadow-lg' 
        : 'bg-[#393D46]/80 backdrop-blur-sm py-4'
    ]"
  >
    <div class="container mx-auto px-4 flex justify-between items-center">
      <!-- Logo on the left -->
      <div class="flex items-center">
        <img src="@/assets/logo.svg" alt="Logo" class="h-12 invert hover:scale-105 transition-transform duration-300" />
      </div>

      <!-- Navigation Links -->
      <nav class="hidden md:flex items-center">
        <a
          v-for="(link, index) in navLinks"
          :key="index"
          :href="link.url"
          class="px-5 py-2 text-white font-medium hover:text-[#FFAE14] transition-all duration-300 relative group mx-1 text-[15px] tracking-wide"
          :class="{ 'active': activeSection === link.url.substring(1) }"
        >
          {{ link.text }}
          <span class="absolute bottom-0 left-0 w-0 h-0.5 bg-[#FFAE14] transition-all duration-300 group-hover:w-full"></span>
        </a>
        
        <!-- Contact Button -->
        <a 
          href="#contacto" 
          class="ml-3 bg-[#FFAE14] hover:bg-[#E7683A] text-white px-5 py-2 rounded-full transition-all duration-300 transform hover:scale-105 font-medium shadow-md text-[15px]"
        >
          Contáctanos
        </a>
      </nav>

      <!-- Mobile Menu Button -->
      <button @click="toggleMobileMenu" class="md:hidden bg-[#FFAE14] text-white px-3 py-1 rounded-full transition-transform duration-300 ease-in-out hover:scale-105 flex items-center">
        <span class="mr-1">Menu</span>
        <svg xmlns="http://www.w3.org/2000/svg" class="h-4 w-4" fill="none" viewBox="0 0 24 24" stroke="currentColor">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16m-7 6h7" />
        </svg>
      </button>
    </div>
    
    <!-- Mobile Menu (Hidden by default) -->
    <div 
      v-if="mobileMenuOpen" 
      class="md:hidden bg-[#393D46] border-t border-[#FFAE14]/20 py-4 px-4 transition-all duration-300 ease-in-out shadow-lg animate-slideDown"
    >
      <a 
        v-for="(link, index) in navLinks" 
        :key="index"
        :href="link.url" 
        class="flex py-2 px-3 mb-1 text-white font-medium hover:bg-[#FFAE14]/10 hover:text-[#FFAE14] rounded transition-colors duration-300 items-center"
        @click="mobileMenuOpen = false"
      >
        <span class="w-1.5 h-1.5 rounded-full bg-[#FFAE14] mr-2"></span>
        {{ link.text }}
      </a>
      
      <!-- Contact Button in Mobile Menu -->
      <a 
        href="#contacto" 
        class="block py-3 px-3 mt-2 bg-[#FFAE14] text-white font-medium rounded transition-colors duration-300 text-center"
        @click="mobileMenuOpen = false"
      >
        Contáctanos
      </a>
    </div>
  </header>
</template>

<script lang="ts">
import { defineComponent, ref, onMounted, onUnmounted } from 'vue'

export default defineComponent({
  name: 'HeaderNavbar',
  setup() {
    const mobileMenuOpen = ref(false)
    const scrolled = ref(false)
    const activeSection = ref('')
    
    const navLinks = [
      { text: 'Inicio', url: '#top' },
      { text: 'Quiénes Somos', url: '#quienes-somos' },
      { text: 'Valores', url: '#valores' },
      { text: 'Servicios', url: '#servicios' },
      { text: 'Reconocimientos', url: '#reconocimientos' }
    ]
    
    const toggleMobileMenu = () => {
      mobileMenuOpen.value = !mobileMenuOpen.value
    }
    
    const handleScroll = () => {
      scrolled.value = window.scrollY > 50
      
      // Determine which section is currently visible
      const sections = document.querySelectorAll('section[id]')
      sections.forEach(section => {
        const sectionElement = section as HTMLElement; // Type assertion to HTMLElement
        const sectionTop = sectionElement.offsetTop - 100;
        const sectionHeight = sectionElement.offsetHeight;
        if (window.scrollY >= sectionTop && window.scrollY < sectionTop + sectionHeight) {
          activeSection.value = section.getAttribute('id') || ''
        }
      })
    }
    
    onMounted(() => {
      window.addEventListener('scroll', handleScroll)
      handleScroll() // Initialize on mount
    })
    
    onUnmounted(() => {
      window.removeEventListener('scroll', handleScroll)
    })
    
    return {
      mobileMenuOpen,
      navLinks,
      toggleMobileMenu,
      scrolled,
      activeSection
    }
  }
})
</script>

<style scoped>
@keyframes fadeIn {
  from { opacity: 0; transform: translateY(-10px); }
  to { opacity: 1; transform: translateY(0); }
}

@keyframes slideDown {
  from { opacity: 0; transform: translateY(-20px); }
  to { opacity: 1; transform: translateY(0); }
}

.animate-slideDown {
  animation: slideDown 0.3s ease-out;
}

.active {
  color: #FFAE14;
}

.active span {
  width: 100%;
}
</style>