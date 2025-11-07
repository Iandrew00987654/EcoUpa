<script setup lang="ts">
const features = ref([
  {
    title: 'Cursos Sostenibles',
    description:
      'Accede a contenidos educativos sobre medio ambiente, energías limpias y desarrollo sostenible, creados por estudiantes con apoyo docente.',
    icon: 'i-lucide-book-open-check',
    to: '/cursos'
  },
  {
    title: 'Aprendizaje Colaborativo',
    description:
      'Conecta con otros participantes para compartir ideas, proyectos e iniciativas ecológicas que promuevan el cambio positivo.',
    icon: 'i-lucide-users',
    to: '/comunidad'
  },
  {
    title: 'Impacto Real',
    description:
      'Participa en actividades y proyectos que generan impacto ambiental y social dentro y fuera de tu comunidad educativa.',
    icon: 'i-lucide-leaf',
    to: '/impacto'
  }
])
</script>

<template>
  <UPageSection
    title="Aprende, colabora y transforma"
    description="EcoUPA ofrece herramientas y contenidos diseñados para impulsar una educación comprometida con la sostenibilidad y el cuidado del planeta."
    :features="features"
  />
</template>
