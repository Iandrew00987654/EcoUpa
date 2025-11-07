<script setup>
const links = ref([
  {
    label: 'Explorar cursos',
    to: '/cursos',
    icon: 'i-lucide-leaf'
  },
  {
    label: 'Saber más',
    to: '/sobre-nosotros',
    color: 'neutral',
    variant: 'subtle',
    trailingIcon: 'i-lucide-arrow-right'
  }
])
</script>
<template>
  <Navbar />

  <UMain>
    <!-- HERO -->
    <UPageCard spotlight  class="pt-10 pb-16">
      <UPageHero title="Educación para un futuro sostenible"
        description="Una plataforma educativa piloto creada por estudiantes y docentes, centrada en la sostenibilidad y el medio ambiente. Aprende, comparte y crea soluciones ecológicas junto a una comunidad comprometida."
        :links="links"
        orientation="horizontal">
       <div class="relative w-full max-w-lg h-64 md:h-80 lg:h-96 overflow-hidden rounded-lg shadow-2xl ring ring-default">
      <img
        src="/assets/main.jpg"
        alt="App main"
        class="absolute inset-0 w-full h-full object-cover"
      />
    </div>
    </UPageHero>
    </UPageCard>

    <!-- MARQUEE / ALIANZAS / PARTNERS -->
    <div class="my-20">
      <UContainer class="flex justify-center items-center">
        <Marquee class="w-full max-w-6xl" />
      </UContainer>
    </div>
    <USeparator class="w-full" />

    <!-- SECCIÓN PRINCIPAL -->
    <UPageBody>
      <SectionMain />
    </UPageBody>
  </UMain>
  <Footer/>
</template>
