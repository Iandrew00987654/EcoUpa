<template>
  <Navbar />

  <UMain class="px-4 py-10">
    <!-- Grid responsive -->
    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
      <!-- Manualmente colocas cada blog -->
      <UBlogPost
        title="Introducción al curso de la Huella Hídrica"
        description="Comprende el impacto del consumo de agua y aprende a medir, reducir y gestionar tu huella hídrica en diferentes contextos."
        image="/huella-hidrica.jpg"
        date="2025-11-06"
        to="/cursos/huellaHidrica"
        orientation="vertical"
      />
      <!-- Curso 2 -->
      <UBlogPost
        title="Reciclaje y residuos"
        description="Aprende sobre gestión de residuos, separación correcta, reciclaje y los fundamentos de la economía circular."
        image="/reciclaje.jpg"
        date="2025-11-06"
        to="/cursos/reciclaje"
        orientation="vertical"
      />

      <!-- Curso 3 -->
      <UBlogPost
        title="Energías renovables"
        description="Explora energía solar, eólica y otras alternativas limpias que están transformando el futuro energético."
        image="/energias-renovables.jpg"
        date="2025-11-06"
        to="/cursos/energiasRenovables"
        orientation="vertical"
      />

      <!-- Curso 4 -->
      <UBlogPost
        title="Cambio climático"
        description="Entiende qué está pasando, cuáles son las causas humanas y naturales, y cómo nos afecta en lo cotidiano."
        image="/cambio-climatico.jpg"
        date="2025-11-06"
        to="/cambioClimatico"
        orientation="vertical"
      />


    </div>
  </UMain>

  <Footer />
</template>