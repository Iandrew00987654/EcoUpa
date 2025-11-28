<template>
  <Navbar />

  <UMain class="py-16 px-4">

    <div class="max-w-6xl mx-auto space-y-14">
      
      <!-- HERO -->
      <section class="text-center space-y-4">
        <h1 class="text-5xl font-extrabold">Sobre Nosotros</h1>

        <p class="text-gray-600 dark:text-gray-300 text-xl max-w-4xl mx-auto">
          EcoUNI nace como un proyecto educativo creado por estudiantes y docentes 
          con la intención de transformar la manera en que aprendemos sobre sostenibilidad. 
          Nuestro objetivo es brindar una plataforma accesible, práctica y capaz de inspirar 
          acciones reales dentro y fuera del aula.
        </p>
      </section>

      <!-- GRID DE TARJETAS -->
      <div class="grid grid-cols-1 md:grid-cols-2 gap-10">

        <!-- MISIÓN -->
        <UPageCard
          title="Nuestra misión"
          spotlight
          icon="i-lucide-graduation-cap"
          description="Construir una plataforma educativa moderna enfocada en sostenibilidad, diseñada para entregar contenido claro, aplicable y relevante para los retos actuales del planeta."
          class="rounded-2xl px-6 py-4 text-lg"
        />

        <!-- CONTENIDO ACCESIBLE -->
        <UPageCard
          title="Contenido accesible"
          spotlight
          icon="i-lucide-laptop"
          description="El material es elaborado por estudiantes comprometidos y revisado con apoyo de docentes y especialistas. Todo está diseñado para que cualquier persona, sin importar su nivel previo, pueda aprender sobre temas ambientales sin complicaciones."
          class="rounded-2xl px-6 py-4 text-lg"
        />

        <!-- APRENDIZAJE COLABORATIVO -->
        <UPageCard
          title="Aprendizaje colaborativo"
          spotlight
          icon="i-lucide-user-round"
          description="Promovemos una comunidad donde todos pueden aportar: experiencias, reflexiones, ideas y soluciones. El aprendizaje no solo viene del contenido, sino de la interacción entre quienes participan."
          class="rounded-2xl px-6 py-4 text-lg"
        />

        <!-- VISIÓN / FUTURO -->
        <UPageCard
          title="Hacia dónde vamos"
          spotlight
          icon="i-lucide-arrow-right"
          description="Planeamos expandir la plataforma con cursos certificados, microaprendizajes, charlas virtuales y alianzas con instituciones académicas y ambientales. EcoUNI busca crecer hasta convertirse en un referente educativo en sostenibilidad."
          class="rounded-2xl px-6 py-6 text-lg"
        />

        <!-- IMPACTO -->
        <UPageCard
          title="Impacto social y ambiental"
          spotlight
          icon="i-lucide-leaf"
          description="Buscamos que el aprendizaje se refleje en acciones reales: desde hábitos personales más responsables hasta proyectos comunitarios con impacto directo. Cada curso y actividad está pensada para impulsar cambios concretos."
          class="rounded-2xl px-6 py-4 text-lg"
        />

        <!-- FUTURO DE LOS ESTUDIANTES -->
        <UPageCard
          title="Formación para el futuro"
          spotlight
          icon="i-lucide-crown"
          description="Más que información, ofrecemos habilidades para que nuevas generaciones comprendan los desafíos ambientales y participen activamente en su solución. Queremos empoderar a estudiantes para convertirse en agentes de cambio."
          class="rounded-2xl px-6 py-4 text-lg"
        />

      </div>

    </div>

  </UMain>

  <Footer />
</template>
