<template>
  <div class="bg-[#E9E9E9]">
    <!-- Header con Navegación -->
    <HeaderNavbar />

    <!-- Hero Section with X decoration background -->
    <section
      id="top"
      class="relative w-full min-h-[650px] bg-[#393D46] overflow-hidden pt-24"
    >
      <!-- X Decoration Background -->
      <XDecoration 
        color="#FFAE14" 
        :thickness="100" 
        :fullScreen="false" 
        :zIndex="1"
        :multipleXs="true"
        :xsCount="8"
        :showParticles="true"
        :particlesCount="15"
      />
      
      <div class="absolute inset-0 flex items-center justify-center z-10">
        <div class="text-center text-white max-w-4xl px-4 animate-hero-content">
          <span class="inline-block text-[#FFAE14] text-lg mb-2 tracking-widest fade-up">BIENVENIDOS A</span>
          <h1 class="text-4xl md:text-6xl font-bold mb-6 tracking-tight text-glow fade-up">
            NEXOS <span class="text-[#FFAE14]">Estrategias</span> & <span class="text-[#E7683A]">Negocios</span>
          </h1>
          <p class="text-xl md:text-2xl mb-8 opacity-90 font-light tracking-wide fade-up">
            Asesoría empresarial integral y especializada
          </p>
          
          <div class="mt-10 fade-up">
            <a href="#contacto" class="inline-block bg-[#FFAE14] hover:bg-[#E7683A] text-white px-8 py-3 rounded-full transition-all duration-300 transform hover:scale-105 font-medium shadow-lg text-lg tracking-wide">
              Solicitar información
            </a>
          </div>
          
          <div class="mt-12 flex justify-center fade-up">
            <div class="space-x-3">
              <span class="inline-block w-3 h-3 rounded-full bg-[#FFAE14] animate-pulse glow-dot"></span>
              <span class="inline-block w-3 h-3 rounded-full bg-[#E7683A] animate-pulse glow-dot" style="animation-delay: 0.2s"></span>
              <span class="inline-block w-3 h-3 rounded-full bg-[#E86934] animate-pulse glow-dot" style="animation-delay: 0.4s"></span>
            </div>
          </div>
        </div>
      </div>
      
      <!-- Scroll indicator -->
      <div class="absolute bottom-6 left-1/2 transform -translate-x-1/2 z-10 animate-bounce" style="animation-duration: 2s">
        <a href="#quienes-somos" class="flex flex-col items-center text-white opacity-70 hover:opacity-100 transition-opacity">
          <span class="text-sm mb-1">Desliza</span>
          <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 14l-7 7m0 0l-7-7m7 7V3" />
          </svg>
        </a>
      </div>
    </section>

    <!-- Quienes Somos Section -->
    <section id="quienes-somos" class="py-16 bg-white">
      <div class="container mx-auto px-4">
        <h2 class="text-3xl font-bold text-center mb-12 text-[#393D46] animate-fade-in">QUIÉNES SOMOS</h2>

        <div class="max-w-4xl mx-auto mb-16 transform transition-all duration-500 hover:scale-105">
          <p class="text-lg text-[#393D46] mb-8 leading-relaxed text-center">
            NEXOS Estrategias & Negocios es una firma de expertos en Administración, Contabilidad,
            Ingeniería Industrial, Finanzas y Derecho. Brindamos consultoría y gestión empresarial
            en áreas fiscal, contable, laboral, legal y comercial para diversos sectores,
            garantizando soluciones estratégicas y eficientes.
          </p>
        </div>
      </div>
    </section>

    <!-- Valores Corporativos Section -->
    <section id="valores">
      <ValoresCarrusel />
    </section>

    <!-- Servicios Section -->
    <section id="servicios" class="py-16 bg-white">
      <div class="container mx-auto px-4">
        <h2 class="text-3xl font-bold text-center mb-12 text-[#393D46] animate-fade-in">NUESTROS SERVICIOS</h2>

        <!-- Línea 1 -->
        <div class="mb-16 animate-fade-in" style="animation-delay: 0.2s">
          <h3
            class="text-2xl font-bold mb-8 text-[#FFAE14] border-b-2 border-[#FFAE14] pb-2 max-w-4xl mx-auto"
          >
            Nexos Negocios – Línea 1
          </h3>

          <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8 max-w-6xl mx-auto">
            <div class="bg-[#E9E9E9] p-6 rounded-lg shadow-md transition-all duration-300 hover:shadow-lg hover:scale-105">
              <h4 class="text-xl font-bold mb-4 text-[#393D46]">01. Gestión Empresarial:</h4>
              <p class="text-[#393D46]">
                ✓ Impulsamos tu negocio con estrategias eficientes, optimizando recursos y equipos
                para maximizar su crecimiento, innovación y sostenibilidad.
              </p>
            </div>

            <div class="bg-[#E9E9E9] p-6 rounded-lg shadow-md transition-all duration-300 hover:shadow-lg hover:scale-105">
              <h4 class="text-xl font-bold mb-4 text-[#393D46]">02. Gestión Laboral:</h4>
              <p class="text-[#393D46]">
                ✓ Asesoría en relaciones laborales, costos salariales, inspecciones y seguridad en
                el trabajo.
              </p>
            </div>

            <div class="bg-[#E9E9E9] p-6 rounded-lg shadow-md transition-all duration-300 hover:shadow-lg hover:scale-105">
              <h4 class="text-xl font-bold mb-4 text-[#393D46]">
                03. Gestión Fiscal y Tributaria:
              </h4>
              <p class="text-[#393D46]">
                ✓ Te ayudamos a optimizar el cumplimiento de tus obligaciones fiscales, reduciendo
                riesgos y mejorando la rentabilidad de tu negocio, siempre dentro del marco legal.
              </p>
            </div>

            <div class="bg-[#E9E9E9] p-6 rounded-lg shadow-md transition-all duration-300 hover:shadow-lg hover:scale-105">
              <h4 class="text-xl font-bold mb-4 text-[#393D46]">04. Gestión Contable:</h4>
              <p class="text-[#393D46]">
                ✓ Mantenemos tus finanzas en orden asegurando el cumplimiento normativo y la toma de
                decisiones inteligentes para el crecimiento de tu negocio.
              </p>
            </div>

            <div class="bg-[#E9E9E9] p-6 rounded-lg shadow-md transition-all duration-300 hover:shadow-lg hover:scale-105">
              <h4 class="text-xl font-bold mb-4 text-[#393D46]">05. Asesoría Legal Empresarial:</h4>
              <p class="text-[#393D46]">
                ✓ Nuestra firma está en capacidad de prestarle servicios en las áreas de derecho
                societario, administrativo, tributario, comercial, civil, contractual, corporativo,
                laboral y procesal.
              </p>
            </div>
          </div>
        </div>

        <!-- Línea 2 -->
        <div class="mb-16 animate-fade-in" style="animation-delay: 0.4s">
          <h3
            class="text-2xl font-bold mb-8 text-[#E7683A] border-b-2 border-[#E7683A] pb-2 max-w-4xl mx-auto"
          >
            Nexos Calidad – Línea 2
          </h3>

          <div class="max-w-4xl mx-auto">
            <div class="bg-[#E9E9E9] p-6 rounded-lg shadow-md transition-all duration-300 hover:shadow-lg hover:scale-105">
              <h4 class="text-xl font-bold mb-4 text-[#393D46]">
                01. Sistema Integrado de Gestión (SIG):
              </h4>
              <p class="text-[#393D46]">
                ✓ Implementación de sistemas integrados de gestión, basados en la trilogía: ISO 9001
                (gestión de calidad), ISO 14001 (gestión ambiental) e ISO 45001 (gestión de
                seguridad y salud ocupacional) o nacionales (Ley 29783 y DS 005).
              </p>
            </div>
          </div>
        </div>

        <!-- Línea 3 -->
        <div class="mb-16 animate-fade-in" style="animation-delay: 0.6s">
          <h3
            class="text-2xl font-bold mb-8 text-[#E86934] border-b-2 border-[#E86934] pb-2 max-w-4xl mx-auto"
          >
            Nexos Legal – Línea 3
          </h3>

          <div class="max-w-4xl mx-auto">
            <div class="bg-[#E9E9E9] p-6 rounded-lg shadow-md transition-all duration-300 hover:shadow-lg hover:scale-105">
              <h4 class="text-xl font-bold mb-4 text-[#393D46]">01. Asesoría Legal Empresarial:</h4>
              <p class="text-[#393D46]">
                ✓ Nuestra firma está en capacidad de prestarle servicios en las áreas del derecho
                societario, administrativo, tributario, comercial, civil, contractual, corporativo,
                laboral y procesal.
              </p>
            </div>
          </div>
        </div>

        <!-- Línea 4 -->
        <div class="mb-16 animate-fade-in" style="animation-delay: 0.8s">
          <h3
            class="text-2xl font-bold mb-8 text-[#FFAE14] border-b-2 border-[#FFAE14] pb-2 max-w-4xl mx-auto"
          >
            Nexos Digital – Línea 4
          </h3>

          <div class="max-w-4xl mx-auto">
            <div class="bg-[#E9E9E9] p-6 rounded-lg shadow-md transition-all duration-300 hover:shadow-lg hover:scale-105">
              <h4 class="text-xl font-bold mb-4 text-[#393D46]">
                01. Tecnología de la Información 🌐:
              </h4>
              <p class="text-[#393D46]">
                ✓ Asesoramos e implementamos soluciones adaptadas a las necesidades específicas de
                cada cliente. Desarrollamos software a medida, hardware especializado y ofrecemos
                servicios TI innovadores. Marketing digital, combinando tecnología y creatividad
                para lograr resultados impactantes.
              </p>
            </div>
          </div>
        </div>

        <!-- Fundación Nexos -->
        <div class="animate-fade-in" style="animation-delay: 1s">
          <h3
            class="text-2xl font-bold mb-8 text-[#E7683A] border-b-2 border-[#E7683A] pb-2 max-w-4xl mx-auto"
          >
            Fundación Nexos
          </h3>

          <div class="grid grid-cols-1 md:grid-cols-2 gap-8 max-w-4xl mx-auto">
            <div class="bg-[#E9E9E9] p-6 rounded-lg shadow-md flex items-center transition-all duration-300 hover:shadow-lg hover:scale-105">
              <div class="text-4xl mr-4 animate-bounce" style="animation-duration: 2s">🎨</div>
              <p class="text-[#393D46] font-medium">¡Proyecto pintando un mundo de esperanzas!</p>
            </div>

            <div class="bg-[#E9E9E9] p-6 rounded-lg shadow-md flex items-center transition-all duration-300 hover:shadow-lg hover:scale-105">
              <div class="text-4xl mr-4 animate-bounce" style="animation-duration: 2.5s; animation-delay: 0.5s">🐾</div>
              <p class="text-[#393D46] font-medium">¡Proyecto échame una pata!</p>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Reconocimientos Section -->
    <section id="reconocimientos" class="py-16 bg-[#E9E9E9]">
      <div class="container mx-auto px-4">
        <h2 class="text-3xl font-bold text-center mb-12 text-[#393D46] animate-fade-in">
          Nuestros Reconocimientos
        </h2>

        <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-8 max-w-6xl mx-auto">
          <!-- ISO 45001 - Ministerio de la Producción -->
          <div class="bg-white p-6 rounded-lg shadow-md transition-all duration-300 hover:shadow-lg hover:scale-105 flex flex-col items-center animate-fade-in" style="animation-delay: 0.1s">
            <div class="h-24 flex items-center justify-center mb-4">
              <img src="/imagenes/ISO_Ministerio_de_la_Producción.png" alt="ISO 45001 - Ministerio de la Producción" class="max-h-24 max-w-full object-contain">
            </div>
            <p class="text-center text-[#393D46] font-medium">
              Certificación ISO 45001 (Ministerio de la Producción)
            </p>
          </div>

          <!-- ISO 45001 - Bureau Veritas -->
          <div class="bg-white p-6 rounded-lg shadow-md transition-all duration-300 hover:shadow-lg hover:scale-105 flex flex-col items-center animate-fade-in" style="animation-delay: 0.2s">
            <div class="h-24 flex items-center justify-center mb-4">
              <img src="/imagenes/iso_45001_Bureau.jpg" alt="ISO 45001 - Bureau Veritas" class="max-h-24 max-w-full object-contain">
            </div>
            <p class="text-center text-[#393D46] font-medium">
              Certificación ISO 45001 (Bureau Veritas Certification)
            </p>
          </div>

          <!-- ProInnóvate -->
          <div class="bg-white p-6 rounded-lg shadow-md transition-all duration-300 hover:shadow-lg hover:scale-105 flex flex-col items-center animate-fade-in" style="animation-delay: 0.3s">
            <div class="h-24 flex items-center justify-center mb-4">
              <img src="/imagenes/logo_proinnovate.png" alt="ProInnóvate" class="max-h-24 max-w-full object-contain">
            </div>
            <p class="text-center text-[#393D46] font-medium">
              Certificación ISO 45001 (Pro Innóvate)
            </p>
          </div>

          <!-- Free Plastic -->
          <div class="bg-white p-6 rounded-lg shadow-md transition-all duration-300 hover:shadow-lg hover:scale-105 flex flex-col items-center animate-fade-in" style="animation-delay: 0.4s">
            <div class="h-24 flex items-center justify-center mb-4">
              <img src="/imagenes/free_plastic.png" alt="Free Plastic" class="max-h-24 max-w-full object-contain">
            </div>
            <p class="text-center text-[#393D46] font-medium">
              Empresa Libre de Plástico (Free Plastic)
            </p>
          </div>

          <!-- SUNAT -->
          <div class="bg-white p-6 rounded-lg shadow-md transition-all duration-300 hover:shadow-lg hover:scale-105 flex flex-col items-center animate-fade-in" style="animation-delay: 0.5s">
            <div class="h-24 flex items-center justify-center mb-4">
              <img src="/imagenes/sunat_logo.png" alt="SUNAT" class="max-h-24 max-w-full object-contain">
            </div>
            <p class="text-center text-[#393D46] font-medium">
              Buenos Contribuyentes (SUNAT)
            </p>
          </div>

          <!-- Cámara de Comercio -->
          <div class="bg-white p-6 rounded-lg shadow-md transition-all duration-300 hover:shadow-lg hover:scale-105 flex flex-col items-center animate-fade-in" style="animation-delay: 0.6s">
            <div class="h-24 flex items-center justify-center mb-4">
              <img src="/imagenes/Camara_comercio_LIMA.jpg" alt="Cámara de Comercio de Lima" class="max-h-24 max-w-full object-contain">
            </div>
            <p class="text-center text-[#393D46] font-medium">
              Asociados: Cámara de Comercio de Lima (CCL)
            </p>
          </div>

          <!-- Ministerio de Trabajo -->
          <div class="bg-white p-6 rounded-lg shadow-md transition-all duration-300 hover:shadow-lg hover:scale-105 flex flex-col items-center animate-fade-in" style="animation-delay: 0.7s">
            <div class="h-24 flex items-center justify-center mb-4">
              <img src="/imagenes/logo_trabajo.jpg" alt="Ministerio de Trabajo" class="max-h-24 max-w-full object-contain">
            </div>
            <p class="text-center text-[#393D46] font-medium">
              Premio Buenas Prácticas Laborales (Ministerio de Trabajo y Promoción del Empleo)
            </p>
          </div>

          <!-- Ministerio del Ambiente - Huella de Carbono -->
          <div class="bg-white p-6 rounded-lg shadow-md transition-all duration-300 hover:shadow-lg hover:scale-105 flex flex-col items-center animate-fade-in" style="animation-delay: 0.8s">
            <div class="h-24 flex items-center justify-center mb-4">
              <img src="/imagenes/ministerio_del_ambiente.png" alt="Ministerio del Ambiente" class="max-h-24 max-w-full object-contain">
            </div>
            <p class="text-center text-[#393D46] font-medium">
              Empresa Ecoeficiente (Ministerio del Ambiente)
            </p>
          </div>

          <!-- Huella de Carbono Perú -->
          <div class="bg-white p-6 rounded-lg shadow-md transition-all duration-300 hover:shadow-lg hover:scale-105 flex flex-col items-center animate-fade-in" style="animation-delay: 0.9s">
            <div class="h-24 flex items-center justify-center mb-4">
              <img src="/imagenes/huella_carbono.jpeg" alt="Huella de Carbono" class="max-h-24 max-w-full object-contain">
            </div>
            <p class="text-center text-[#393D46] font-medium">
              Certificación Huella de Carbono (Perú)
            </p>
          </div>

          <!-- Pontificia Universidad Católica del Perú -->
          <div class="bg-white p-6 rounded-lg shadow-md transition-all duration-300 hover:shadow-lg hover:scale-105 flex flex-col items-center animate-fade-in" style="animation-delay: 1s">
            <div class="h-24 flex items-center justify-center mb-4">
              <img src="/imagenes/Pontificia_Catolica.jpg" alt="PUCP" class="max-h-24 max-w-full object-contain">
            </div>
            <p class="text-center text-[#393D46] font-medium">
              Certificación Programa 5'S (Pontificia Universidad Católica del Perú)
            </p>
          </div>

          <!-- Homologados Alicorp -->
          <div class="bg-white p-6 rounded-lg shadow-md transition-all duration-300 hover:shadow-lg hover:scale-105 flex flex-col items-center animate-fade-in" style="animation-delay: 1.1s">
            <div class="h-24 flex items-center justify-center mb-4">
              <img src="/imagenes/Alicorp_logo.png" alt="Alicorp" class="max-h-24 max-w-full object-contain">
            </div>
            <p class="text-center text-[#393D46] font-medium">
              Homologados: Alicorp
            </p>
          </div>

          <!-- Homologados Carso -->
          <div class="bg-white p-6 rounded-lg shadow-md transition-all duration-300 hover:shadow-lg hover:scale-105 flex flex-col items-center animate-fade-in" style="animation-delay: 1.2s">
            <div class="h-24 flex items-center justify-center mb-4">
              <img src="/imagenes/carso.webp" alt="Carso" class="max-h-24 max-w-full object-contain">
            </div>
            <p class="text-center text-[#393D46] font-medium">
              Homologados: Carso
            </p>
          </div>
        </div>
      </div>
    </section>

    <!-- Contact Section -->
    <section id="contacto" class="py-16 bg-white">
      <div class="container mx-auto px-4">
        <h2 class="text-3xl font-bold text-center mb-12 text-[#393D46] animate-fade-in">Información de Contacto</h2>

        <div class="grid grid-cols-1 md:grid-cols-2 gap-8 max-w-5xl mx-auto">
          <!-- Contact Information -->
          <div class="bg-[#E9E9E9] p-8 rounded-lg shadow-md transform transition-all duration-500 hover:scale-105">
            <div class="space-y-6">
              <div class="flex items-start transition-transform duration-300 hover:translate-x-2">
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  class="h-6 w-6 text-[#FFAE14] mr-3"
                  fill="none"
                  viewBox="0 0 24 24"
                  stroke="currentColor"
                >
                  <path
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    stroke-width="2"
                    d="M3 5a2 2 0 012-2h3.28a1 1 0 01.948.684l1.498 4.493a1 1 0 01-.502 1.21l-2.257 1.13a11.042 11.042 0 005.516 5.516l1.13-2.257a1 1 0 011.21-.502l4.493 1.498a1 1 0 01.684.949V19a2 2 0 01-2 2h-1C9.716 21 3 14.284 3 6V5z"
                  />
                </svg>
                <div>
                  <p class="font-bold text-[#393D46]">Central:</p>
                  <p class="text-[#393D46]">(051) 909-2347</p>
                </div>
              </div>

              <div class="flex items-start transition-transform duration-300 hover:translate-x-2">
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  class="h-6 w-6 text-[#E7683A] mr-3"
                  fill="none"
                  viewBox="0 0 24 24"
                  stroke="currentColor"
                >
                  <path
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    stroke-width="2"
                    d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"
                  />
                </svg>
                <div>
                  <p class="font-bold text-[#393D46]">Email:</p>
                  <p class="text-[#393D46]">abaldeon@asesoriaennegocios.com</p>
                  <p class="text-[#393D46]">vbaldeon@asesoriaennegocios.com</p>
                </div>
              </div>

              <div class="flex items-start transition-transform duration-300 hover:translate-x-2">
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  class="h-6 w-6 text-[#E86934] mr-3"
                  fill="none"
                  viewBox="0 0 24 24"
                  stroke="currentColor"
                >
                  <path
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    stroke-width="2"
                    d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z"
                  />
                  <path
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    stroke-width="2"
                    d="M15 11a3 3 0 11-6 0 3 3 0 016 0z"
                  />
                </svg>
                <div>
                  <p class="font-bold text-[#393D46]">Ubicación:</p>
                  <p class="text-[#393D46]">Lima 043 - Perú</p>
                </div>
              </div>

              <div class="flex items-start transition-transform duration-300 hover:translate-x-2">
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  class="h-6 w-6 text-[#FFAE14] mr-3"
                  fill="none"
                  viewBox="0 0 24 24"
                  stroke="currentColor"
                >
                  <path
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    stroke-width="2"
                    d="M8 12h.01M12 12h.01M16 12h.01M21 12c0 4.418-4.03 8-9 8a9.863 9.863 0 01-4.255-.949L3 20l1.395-3.72C3.512 15.042 3 13.574 3 12c0-4.418 4.03-8 9-8s9 3.582 9 8z"
                  />
                </svg>
                <div>
                  <p class="font-bold text-[#393D46]">WhatsApp:</p>
                  <p class="text-[#393D46]">998 261 424</p>
                  <p class="text-[#393D46]">987 934 513</p>
                </div>
              </div>

              <div class="flex items-start transition-transform duration-300 hover:translate-x-2">
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  class="h-6 w-6 text-[#E7683A] mr-3"
                  fill="none"
                  viewBox="0 0 24 24"
                  stroke="currentColor"
                >
                  <path
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    stroke-width="2"
                    d="M21 12a9 9 0 01-9 9m9-9a9 9 0 00-9-9m9 9H3m9 9a9 9 0 01-9-9m9 9c1.657 0 3-4.03 3-9s-1.343-9-3-9m0 18c-1.657 0-3-4.03-3-9s1.343-9 3-9m-9 9a9 9 0 019-9"
                  />
                </svg>
                <div>
                  <p class="font-bold text-[#393D46]">Web:</p>
                  <p class="text-[#393D46]">www.asesoriaennegocios.com</p>
                </div>
              </div>
            </div>

            <h4 class="text-xl font-semibold mt-8 mb-4 text-[#393D46]">Síguenos en:</h4>
            <div class="flex space-x-4">
              <a href="#" class="text-[#FFAE14] hover:text-[#E7683A] transition-colors duration-300 transform hover:scale-125">
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  class="h-6 w-6"
                  fill="currentColor"
                  viewBox="0 0 24 24"
                >
                  <path
                    d="M9 8h-3v4h3v12h5v-12h3.642l.358-4h-4v-1.667c0-.955.192-1.333 1.115-1.333h2.885v-5h-3.808c-3.596 0-5.192 1.583-5.192 4.615v3.385z"
                  />
                </svg>
              </a>
              <a href="#" class="text-[#FFAE14] hover:text-[#E7683A] transition-colors duration-300 transform hover:scale-125">
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  class="h-6 w-6"
                  fill="currentColor"
                  viewBox="0 0 24 24"
                >
                  <path
                    d="M4.98 3.5c0 1.381-1.11 2.5-2.48 2.5s-2.48-1.119-2.48-2.5c0-1.38 1.11-2.5 2.48-2.5s2.48 1.12 2.48 2.5zm.02 4.5h-5v16h5v-16zm7.982 0h-4.968v16h4.969v-8.399c0-4.67 6.029-5.052 6.029 0v8.399h4.988v-10.131c0-7.88-8.922-7.593-11.018-3.714v-2.155z"
                  />
                </svg>
              </a>
              <a href="#" class="text-[#FFAE14] hover:text-[#E7683A] transition-colors duration-300 transform hover:scale-125">
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  class="h-6 w-6"
                  fill="currentColor"
                  viewBox="0 0 24 24"
                >
                  <path
                    d="M12 2.163c3.204 0 3.584.012 4.85.07 3.252.148 4.771 1.691 4.919 4.919.058 1.265.069 1.645.069 4.849 0 3.205-.012 3.584-.069 4.849-.149 3.225-1.664 4.771-4.919 4.919-1.266.058-1.644.07-4.85.07-3.204 0-3.584-.012-4.849-.07-3.26-.149-4.771-1.699-4.919-4.92-.058-1.265-.07-1.644-.07-4.849 0-3.204.013-3.583.07-4.849.149-3.227 1.664-4.771 4.919-4.919 1.266-.057 1.645-.069 4.849-.069zm0-2.163c-3.259 0-3.667.014-4.947.072-4.358.2-6.78 2.618-6.98 6.98-.059 1.281-.073 1.689-.073 4.948 0 3.259.014 3.668.072 4.948.2 4.358 2.618 6.78 6.98 6.98 1.281.058 1.689.072 4.948.072 3.259 0 3.668-.014 4.948-.072 4.354-.2 6.782-2.618 6.979-6.98.059-1.28.073-1.689.073-4.948 0-3.259-.014-3.667-.072-4.947-.196-4.354-2.617-6.78-6.979-6.98-1.281-.059-1.69-.073-4.949-.073zm0 5.838c-3.403 0-6.162 2.759-6.162 6.162s2.759 6.163 6.162 6.163 6.162-2.759 6.162-6.163c0-3.403-2.759-6.162-6.162-6.162zm0 10.162c-2.209 0-4-1.79-4-4 0-2.209 1.791-4 4-4s4 1.791 4 4c0 2.21-1.791 4-4 4zm6.406-11.845c-.796 0-1.441.645-1.441 1.44s.645 1.44 1.441 1.44c.795 0 1.439-.645 1.439-1.44s-.644-1.44-1.439-1.44z"
                  />
                </svg>
              </a>
              <a href="#" class="text-[#FFAE14] hover:text-[#E7683A] transition-colors duration-300 transform hover:scale-125">
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  class="h-6 w-6"
                  fill="currentColor"
                  viewBox="0 0 24 24"
                >
                  <path
                    d="M19.615 3.184c-3.604-.246-11.631-.245-15.23 0-3.897.266-4.356 2.62-4.385 8.816.029 6.185.484 8.549 4.385 8.816 3.6.245 11.626.246 15.23 0 3.897-.266 4.356-2.62 4.385-8.816-.029-6.185-.484-8.549-4.385-8.816zm-10.615 12.816v-8l8 3.993-8 4.007z"
                  />
                </svg>
              </a>
            </div>
          </div>

          <!-- Map Image Placeholder -->
          <div class="h-full min-h-[400px] bg-[#E9E9E9] rounded-lg shadow-md overflow-hidden transform transition-all duration-500 hover:scale-105">
            <iframe
              src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d249743.7236882099!2d-77.15345344353724!3d-12.02671962441933!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x9105c5f619ee3ec7%3A0x14206cb9cc452e4a!2sLima%2C%20Peru!5e0!3m2!1sen!2ses!4v1650137644266!5m2!1sen!2ses"
              width="100%"
              height="100%"
              style="border: 0"
              allowfullscreen
              loading="lazy"
              referrerpolicy="no-referrer-when-downgrade"
            >
            </iframe>
          </div>
        </div>
      </div>
    </section>

    <!-- Footer -->
    <FooterComponent />
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import HeaderNavbar from '@/components/layout/HeaderNavbar.vue'
import FooterComponent from '@/components/layout/FooterComponent.vue'
import ValoresCarrusel from '@/components/ValoresCarrusel.vue'
import XDecoration from '@/components/XDecoration.vue'

export default defineComponent({
  name: 'LandingPage',
  components: {
    HeaderNavbar,
    FooterComponent,
    ValoresCarrusel,
    XDecoration
  }
})
</script>

<style scoped>
.animate-fade-in {
  animation: fadeIn 1s ease-in-out;
}

.animate-hero-content {
  animation: heroContent 1.2s ease-out;
}

.animate-bounce {
  animation: bounce 2s infinite;
}

.animate-pulse {
  animation: pulse 2s cubic-bezier(0.4, 0, 0.6, 1) infinite;
}

.text-glow {
  text-shadow: 0 0 8px rgba(255, 255, 255, 0.8), 0 0 16px rgba(255, 255, 255, 0.6);
}

.glow-dot {
  box-shadow: 0 0 8px rgba(255, 255, 255, 0.8), 0 0 16px rgba(255, 255, 255, 0.6);
}

@keyframes fadeIn {
  from { opacity: 0; transform: translateY(20px); }
  to { opacity: 1; transform: translateY(0); }
}

@keyframes heroContent {
  0% { opacity: 0; transform: scale(0.9); }
  30% { opacity: 0.5; transform: scale(1.05); }
  100% { opacity: 1; transform: scale(1); }
}

@keyframes bounce {
  0%, 100% { transform: translateY(0); }
  50% { transform: translateY(-10px); }
}

@keyframes pulse {
  0%, 100% { opacity: 1; }
  50% { opacity: .5; }
}
</style>
