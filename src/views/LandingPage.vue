<template>
  <div class="bg-[#E9E9E9]">
    <!-- Header with Navigation Bar -->
    <header class="w-full bg-white shadow-sm">
      <div class="container mx-auto px-4 py-2 flex justify-between items-center">
        <!-- Logo on the left -->
        <div class="flex items-center">
          <img src="@/assets/logo.svg" alt="Logo" class="h-12" />
        </div>

        <!-- Navigation Links -->
        <nav class="hidden md:flex items-center space-x-1">
          <a
            href="#quienes-somos"
            class="px-3 py-2 text-[#393D46] font-medium hover:bg-[#FFAE14]/10 rounded"
            >Quiénes Somos</a
          >
          <a
            href="#servicios"
            class="px-3 py-2 text-[#393D46] font-medium hover:bg-[#FFAE14]/10 rounded"
            >Servicios</a
          >
          <a
            href="#valores"
            class="px-3 py-2 text-[#393D46] font-medium hover:bg-[#FFAE14]/10 rounded"
            >Valores</a
          >
          <a
            href="#reconocimientos"
            class="px-3 py-2 text-[#393D46] font-medium hover:bg-[#FFAE14]/10 rounded"
            >Reconocimientos</a
          >
          <a
            href="#contacto"
            class="px-3 py-2 text-[#393D46] font-medium hover:bg-[#FFAE14]/10 rounded"
            >Contacto</a
          >
        </nav>

        <!-- Mobile Menu Button -->
        <button class="md:hidden bg-[#FFAE14] text-white px-3 py-1 rounded">Menu</button>
      </div>
    </header>

    <!-- Hero Section with Background Image -->
    <section
      class="relative w-full h-[500px] bg-cover bg-center"
      style="
        background-image: url('https://images.unsplash.com/photo-1600880292203-757bb62b4baf?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1770&q=80');
      "
    >
      <div class="absolute inset-0 bg-[#393D46] bg-opacity-70 flex items-center justify-center">
        <div class="text-center text-white">
          <h1 class="text-4xl md:text-5xl font-bold mb-4">NEXOS Estrategias & Negocios</h1>
          <p class="text-xl mb-6">Asesoría empresarial integral y especializada</p>
          <div class="flex justify-center">
            <div class="space-x-2">
              <span class="inline-block w-2 h-2 rounded-full bg-[#FFAE14]"></span>
              <span class="inline-block w-2 h-2 rounded-full bg-[#E7683A]"></span>
              <span class="inline-block w-2 h-2 rounded-full bg-[#E86934]"></span>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Quienes Somos Section -->
    <section id="quienes-somos" class="py-16 bg-white">
      <div class="container mx-auto px-4">
        <h2 class="text-3xl font-bold text-center mb-12 text-[#393D46]">QUIÉNES SOMOS</h2>

        <div class="max-w-4xl mx-auto mb-16">
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
    <section id="valores" class="py-16 bg-[#E9E9E9]">
      <div class="container mx-auto px-4">
        <h2 class="text-3xl font-bold text-center mb-12 text-[#393D46]">Valores Corporativos</h2>

        <div class="grid grid-cols-1 md:grid-cols-2 gap-8 max-w-5xl mx-auto">
          <div class="bg-white p-8 rounded-lg shadow-md flex flex-col">
            <div class="text-[#FFAE14] mb-3 text-5xl font-serif">"</div>
            <p class="text-[#393D46] mb-4 italic text-lg">
              La disciplina es el puente entre las metas y el logro
            </p>
            <div class="mt-auto text-[#E7683A] font-semibold">- Jim Rohn</div>
          </div>

          <div class="bg-white p-8 rounded-lg shadow-md flex flex-col">
            <div class="text-[#FFAE14] mb-3 text-5xl font-serif">"</div>
            <p class="text-[#393D46] mb-4 italic text-lg">
              La integridad es hacer lo correcto aunque nadie esté mirando
            </p>
            <div class="mt-auto text-[#E7683A] font-semibold">- Jim Stovall</div>
          </div>

          <div class="bg-white p-8 rounded-lg shadow-md flex flex-col">
            <div class="text-[#FFAE14] mb-3 text-5xl font-serif">"</div>
            <p class="text-[#393D46] mb-4 italic text-lg">
              La innovación constante es la única forma de mantenerse competitivo a largo plazo
            </p>
            <div class="mt-auto text-[#E7683A] font-semibold">- Jorge Gonzales</div>
          </div>

          <div class="bg-white p-8 rounded-lg shadow-md flex flex-col">
            <div class="text-[#FFAE14] mb-3 text-5xl font-serif">"</div>
            <p class="text-[#393D46] mb-4 italic text-lg">
              La confidencialidad es una virtud de la lealtad, la lealtad es la virtud de la
              fidelidad
            </p>
            <div class="mt-auto text-[#E7683A] font-semibold">- Edwin Louis</div>
          </div>
        </div>
      </div>
    </section>

    <!-- Servicios Section -->
    <section id="servicios" class="py-16 bg-white">
      <div class="container mx-auto px-4">
        <h2 class="text-3xl font-bold text-center mb-12 text-[#393D46]">NUESTROS SERVICIOS</h2>

        <!-- Línea 1 -->
        <div class="mb-16">
          <h3
            class="text-2xl font-bold mb-8 text-[#FFAE14] border-b-2 border-[#FFAE14] pb-2 max-w-4xl mx-auto"
          >
            Nexos Negocios – Línea 1
          </h3>

          <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8 max-w-6xl mx-auto">
            <div class="bg-[#E9E9E9] p-6 rounded-lg shadow-md">
              <h4 class="text-xl font-bold mb-4 text-[#393D46]">01. Gestión Empresarial:</h4>
              <p class="text-[#393D46]">
                ✓ Impulsamos tu negocio con estrategias eficientes, optimizando recursos y equipos
                para maximizar su crecimiento, innovación y sostenibilidad.
              </p>
            </div>

            <div class="bg-[#E9E9E9] p-6 rounded-lg shadow-md">
              <h4 class="text-xl font-bold mb-4 text-[#393D46]">02. Gestión Laboral:</h4>
              <p class="text-[#393D46]">
                ✓ Asesoría en relaciones laborales, costos salariales, inspecciones y seguridad en
                el trabajo.
              </p>
            </div>

            <div class="bg-[#E9E9E9] p-6 rounded-lg shadow-md">
              <h4 class="text-xl font-bold mb-4 text-[#393D46]">
                03. Gestión Fiscal y Tributaria:
              </h4>
              <p class="text-[#393D46]">
                ✓ Te ayudamos a optimizar el cumplimiento de tus obligaciones fiscales, reduciendo
                riesgos y mejorando la rentabilidad de tu negocio, siempre dentro del marco legal.
              </p>
            </div>

            <div class="bg-[#E9E9E9] p-6 rounded-lg shadow-md">
              <h4 class="text-xl font-bold mb-4 text-[#393D46]">04. Gestión Contable:</h4>
              <p class="text-[#393D46]">
                ✓ Mantenemos tus finanzas en orden asegurando el cumplimiento normativo y la toma de
                decisiones inteligentes para el crecimiento de tu negocio.
              </p>
            </div>

            <div class="bg-[#E9E9E9] p-6 rounded-lg shadow-md">
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
        <div class="mb-16">
          <h3
            class="text-2xl font-bold mb-8 text-[#E7683A] border-b-2 border-[#E7683A] pb-2 max-w-4xl mx-auto"
          >
            Nexos Calidad – Línea 2
          </h3>

          <div class="max-w-4xl mx-auto">
            <div class="bg-[#E9E9E9] p-6 rounded-lg shadow-md">
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
        <div class="mb-16">
          <h3
            class="text-2xl font-bold mb-8 text-[#E86934] border-b-2 border-[#E86934] pb-2 max-w-4xl mx-auto"
          >
            Nexos Legal – Línea 3
          </h3>

          <div class="max-w-4xl mx-auto">
            <div class="bg-[#E9E9E9] p-6 rounded-lg shadow-md">
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
        <div class="mb-16">
          <h3
            class="text-2xl font-bold mb-8 text-[#FFAE14] border-b-2 border-[#FFAE14] pb-2 max-w-4xl mx-auto"
          >
            Nexos Digital – Línea 4
          </h3>

          <div class="max-w-4xl mx-auto">
            <div class="bg-[#E9E9E9] p-6 rounded-lg shadow-md">
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
        <div>
          <h3
            class="text-2xl font-bold mb-8 text-[#E7683A] border-b-2 border-[#E7683A] pb-2 max-w-4xl mx-auto"
          >
            Fundación Nexos
          </h3>

          <div class="grid grid-cols-1 md:grid-cols-2 gap-8 max-w-4xl mx-auto">
            <div class="bg-[#E9E9E9] p-6 rounded-lg shadow-md flex items-center">
              <div class="text-4xl mr-4">🎨</div>
              <p class="text-[#393D46] font-medium">¡Proyecto pintando un mundo de esperanzas!</p>
            </div>

            <div class="bg-[#E9E9E9] p-6 rounded-lg shadow-md flex items-center">
              <div class="text-4xl mr-4">🐾</div>
              <p class="text-[#393D46] font-medium">¡Proyecto échame una pata!</p>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Reconocimientos Section -->
    <section id="reconocimientos" class="py-16 bg-[#E9E9E9]">
      <div class="container mx-auto px-4">
        <h2 class="text-3xl font-bold text-center mb-12 text-[#393D46]">
          Nuestros Reconocimientos
        </h2>

        <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-6 max-w-5xl mx-auto">
          <div class="bg-white p-4 rounded-lg shadow-md">
            <div class="h-14 flex items-center justify-center text-[#FFAE14]">
              <svg
                xmlns="http://www.w3.org/2000/svg"
                class="h-10 w-10"
                fill="none"
                viewBox="0 0 24 24"
                stroke="currentColor"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="2"
                  d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z"
                />
              </svg>
            </div>
            <p class="text-center text-[#393D46] font-medium">
              Certificación ISO 45001 (Ministerio de la Producción)
            </p>
          </div>

          <div class="bg-white p-4 rounded-lg shadow-md">
            <div class="h-14 flex items-center justify-center text-[#FFAE14]">
              <svg
                xmlns="http://www.w3.org/2000/svg"
                class="h-10 w-10"
                fill="none"
                viewBox="0 0 24 24"
                stroke="currentColor"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="2"
                  d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z"
                />
              </svg>
            </div>
            <p class="text-center text-[#393D46] font-medium">
              Certificación ISO 45001 (Bureau Veritas Certification)
            </p>
          </div>

          <div class="bg-white p-4 rounded-lg shadow-md">
            <div class="h-14 flex items-center justify-center text-[#FFAE14]">
              <svg
                xmlns="http://www.w3.org/2000/svg"
                class="h-10 w-10"
                fill="none"
                viewBox="0 0 24 24"
                stroke="currentColor"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="2"
                  d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z"
                />
              </svg>
            </div>
            <p class="text-center text-[#393D46] font-medium">
              Certificación ISO 45001 (Pro Innóvate)
            </p>
          </div>

          <div class="bg-white p-4 rounded-lg shadow-md">
            <div class="h-14 flex items-center justify-center text-[#E7683A]">
              <svg
                xmlns="http://www.w3.org/2000/svg"
                class="h-10 w-10"
                fill="none"
                viewBox="0 0 24 24"
                stroke="currentColor"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="2"
                  d="M7 21a4 4 0 01-4-4V5a2 2 0 012-2h4a2 2 0 012 2v12a4 4 0 01-4 4zm0 0h12a2 2 0 002-2v-4a2 2 0 00-2-2h-2.343M11 7.343l1.657-1.657a2 2 0 012.828 0l2.829 2.829a2 2 0 010 2.828l-8.486 8.485M7 17h.01"
                />
              </svg>
            </div>
            <p class="text-center text-[#393D46] font-medium">
              Empresa Libre de Plástico (Free Plastic)
            </p>
          </div>

          <div class="bg-white p-4 rounded-lg shadow-md">
            <div class="h-14 flex items-center justify-center text-[#E7683A]">
              <svg
                xmlns="http://www.w3.org/2000/svg"
                class="h-10 w-10"
                fill="none"
                viewBox="0 0 24 24"
                stroke="currentColor"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="2"
                  d="M12 8c-1.657 0-3 .895-3 2s1.343 2 3 2 3 .895 3 2-1.343 2-3 2m0-8c1.11 0 2.08.402 2.599 1M12 8V7m0 1v8m0 0v1m0-1c-1.11 0-2.08-.402-2.599-1M21 12a9 9 0 11-18 0 9 9 0 0118 0z"
                />
              </svg>
            </div>
            <p class="text-center text-[#393D46] font-medium">Buenos Contribuyentes (SUNAT)</p>
          </div>

          <div class="bg-white p-4 rounded-lg shadow-md">
            <div class="h-14 flex items-center justify-center text-[#E7683A]">
              <svg
                xmlns="http://www.w3.org/2000/svg"
                class="h-10 w-10"
                fill="none"
                viewBox="0 0 24 24"
                stroke="currentColor"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="2"
                  d="M17 20h5v-2a3 3 0 00-5.356-1.857M17 20H7m10 0v-2c0-.656-.126-1.283-.356-1.857M7 20H2v-2a3 3 0 015.356-1.857M7 20v-2c0-.656.126-1.283.356-1.857m0 0a5.002 5.002 0 019.288 0M15 7a3 3 0 11-6 0 3 3 0 016 0zm6 3a2 2 0 11-4 0 2 2 0 014 0zM7 10a2 2 0 11-4 0 2 2 0 014 0z"
                />
              </svg>
            </div>
            <p class="text-center text-[#393D46] font-medium">
              Asociados: Cámara de Comercio de Lima (CCL)
            </p>
          </div>

          <div class="bg-white p-4 rounded-lg shadow-md">
            <div class="h-14 flex items-center justify-center text-[#E86934]">
              <svg
                xmlns="http://www.w3.org/2000/svg"
                class="h-10 w-10"
                fill="none"
                viewBox="0 0 24 24"
                stroke="currentColor"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="2"
                  d="M21 13.255A23.931 23.931 0 0112 15c-3.183 0-6.22-.62-9-1.745M16 6V4a2 2 0 00-2-2h-4a2 2 0 00-2 2v2m4 6h.01M5 20h14a2 2 0 002-2V8a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"
                />
              </svg>
            </div>
            <p class="text-center text-[#393D46] font-medium">
              Premio Buenas Prácticas Laborales (Ministerio de Trabajo y Promoción del Empleo)
            </p>
          </div>

          <div class="bg-white p-4 rounded-lg shadow-md">
            <div class="h-14 flex items-center justify-center text-[#E86934]">
              <svg
                xmlns="http://www.w3.org/2000/svg"
                class="h-10 w-10"
                fill="none"
                viewBox="0 0 24 24"
                stroke="currentColor"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="2"
                  d="M3.055 11H5a2 2 0 012 2v1a2 2 0 002 2 2 2 0 012 2v2.945M8 3.935V5.5A2.5 2.5 0 0010.5 8h.5a2 2 0 012 2 2 2 0 104 0 2 2 0 012-2h.5A2.5 2.5 0 0020 5.5v-1.5"
                />
              </svg>
            </div>
            <p class="text-center text-[#393D46] font-medium">
              Empresa Ecoeficiente (Huella de Carbono - Perú)
            </p>
          </div>

          <div class="bg-white p-4 rounded-lg shadow-md">
            <div class="h-14 flex items-center justify-center text-[#E86934]">
              <svg
                xmlns="http://www.w3.org/2000/svg"
                class="h-10 w-10"
                fill="none"
                viewBox="0 0 24 24"
                stroke="currentColor"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="2"
                  d="M19.428 15.428a2 2 0 00-1.022-.547l-2.387-.477a6 6 0 00-3.86.517l-.318.158a6 6 0 01-3.86.517L6.05 15.21a2 2 0 00-1.806.547M8 4h8l-1 1v5.172a2 2 0 00.586 1.414l5 5c1.26 1.26.367 3.414-1.415 3.414H4.828c-1.782 0-2.674-2.154-1.414-3.414l5-5A2 2 0 009 10.172V5L8 4z"
                />
              </svg>
            </div>
            <p class="text-center text-[#393D46] font-medium">
              Certificación Programa 5'S (Pontificia Universidad Católica del Perú)
            </p>
          </div>

          <div class="bg-white p-4 rounded-lg shadow-md">
            <div class="h-14 flex items-center justify-center text-[#FFAE14]">
              <svg
                xmlns="http://www.w3.org/2000/svg"
                class="h-10 w-10"
                fill="none"
                viewBox="0 0 24 24"
                stroke="currentColor"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="2"
                  d="M9 12l2 2 4-4M7.835 4.697a3.42 3.42 0 001.946-.806 3.42 3.42 0 014.438 0 3.42 3.42 0 001.946.806 3.42 3.42 0 013.138 3.138 3.42 3.42 0 00.806 1.946 3.42 3.42 0 010 4.438 3.42 3.42 0 00-.806 1.946 3.42 3.42 0 01-3.138 3.138 3.42 3.42 0 00-1.946.806 3.42 3.42 0 01-4.438 0 3.42 3.42 0 00-1.946-.806 3.42 3.42 0 01-3.138-3.138 3.42 3.42 0 00-.806-1.946 3.42 3.42 0 010-4.438 3.42 3.42 0 00.806-1.946 3.42 3.42 0 013.138-3.138z"
                />
              </svg>
            </div>
            <p class="text-center text-[#393D46] font-medium">Homologados: Alicorp / Carso</p>
          </div>

          <div class="bg-white p-4 rounded-lg shadow-md">
            <div class="h-14 flex items-center justify-center text-[#FFAE14]">
              <svg
                xmlns="http://www.w3.org/2000/svg"
                class="h-10 w-10"
                fill="none"
                viewBox="0 0 24 24"
                stroke="currentColor"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="2"
                  d="M3.055 11H5a2 2 0 012 2v1a2 2 0 002 2 2 2 0 012 2v2.945M8 3.935V5.5A2.5 2.5 0 0010.5 8h.5a2 2 0 012 2 2 2 0 104 0 2 2 0 012-2h.5A2.5 2.5 0 0020 5.5v-1.5"
                />
              </svg>
            </div>
            <p class="text-center text-[#393D46] font-medium">
              Empresa Ecoeficiente (Ministerio del Ambiente)
            </p>
          </div>
        </div>
      </div>
    </section>

    <!-- Contact Section -->
    <section id="contacto" class="py-16 bg-white">
      <div class="container mx-auto px-4">
        <h2 class="text-3xl font-bold text-center mb-12 text-[#393D46]">Información de Contacto</h2>

        <div class="grid grid-cols-1 md:grid-cols-2 gap-8 max-w-5xl mx-auto">
          <!-- Contact Information -->
          <div class="bg-[#E9E9E9] p-8 rounded-lg shadow-md">
            <div class="space-y-6">
              <div class="flex items-start">
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

              <div class="flex items-start">
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

              <div class="flex items-start">
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

              <div class="flex items-start">
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

              <div class="flex items-start">
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
              <a href="#" class="text-[#FFAE14] hover:text-[#E7683A]">
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
              <a href="#" class="text-[#FFAE14] hover:text-[#E7683A]">
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
              <a href="#" class="text-[#FFAE14] hover:text-[#E7683A]">
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
              <a href="#" class="text-[#FFAE14] hover:text-[#E7683A]">
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
          <div class="h-full min-h-[400px] bg-[#E9E9E9] rounded-lg shadow-md overflow-hidden">
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
    <footer class="bg-[#393D46] text-white py-8">
      <div class="container mx-auto px-4">
        <div class="flex flex-col md:flex-row justify-between items-center">
          <div class="mb-4 md:mb-0">
            <p>&copy; 2025 NEXOS Estrategias & Negocios. Todos los derechos reservados.</p>
          </div>

          <div class="flex items-center">
            <img src="@/assets/logo.svg" alt="Logo" class="h-8 mr-2 invert" />
            <div class="text-sm">
              <p>Una firma de expertos</p>
              <p>Sirviendo desde 2025</p>
            </div>
          </div>
        </div>
      </div>
    </footer>
  </div>
</template>

<script lang="ts">
export default {
  name: 'LandingPage',
}
</script>
