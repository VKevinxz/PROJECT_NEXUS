<script setup lang="ts">
import { RouterView } from 'vue-router'
import { onMounted } from 'vue'

// Script para activar animaciones al hacer scroll
onMounted(() => {
  const observerOptions = {
    root: null,
    rootMargin: '0px',
    threshold: 0.15
  }

  const handleIntersect = (entries: IntersectionObserverEntry[], observer: IntersectionObserver) => {
    entries.forEach(entry => {
      if (entry.isIntersecting) {
        entry.target.classList.add('appear')
        observer.unobserve(entry.target)
      }
    })
  }

  // Crear el observer para elementos con animación
  const observer = new IntersectionObserver(handleIntersect, observerOptions)
  
  // Observar todos los elementos con la clase fade-up
  document.querySelectorAll('.fade-up').forEach(el => {
    observer.observe(el)
  })

  // Añadir un ID al primer section para la navegación
  const firstSection = document.querySelector('section')
  if (firstSection && !firstSection.id) {
    firstSection.id = 'top'
  }
})
</script>

<template>
  <RouterView />
</template>

<style>
/* Ajustes para fuentes en diferentes elementos */
h1, h2, h3, h4, h5, h6 {
  font-family: var(--font-secondary);
}

body, p, span, a, button, input, textarea, li {
  font-family: var(--font-primary);
}

/* Optimizaciones de rendimiento */
img, svg {
  transition: transform 0.3s ease;
}

/* Mejorar legibilidad */
p {
  max-width: 70ch;
  margin-left: auto;
  margin-right: auto;
}

/* Estilos útiles para todas las páginas */
.container {
  max-width: 1280px;
  margin: 0 auto;
  padding: 0 1rem;
}

@media (max-width: 768px) {
  h1 {
    font-size: 2rem !important;
  }
  
  h2 {
    font-size: 1.75rem !important;
  }
}
</style>
