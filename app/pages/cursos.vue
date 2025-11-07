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
        to="#"
        orientation="vertical"
      />


    </div>
  </UMain>

  <Footer />
</template>