<script setup lang="ts">
import type { NavigationMenuItem } from '@nuxt/ui'
const router = useRouter()

const items = computed<NavigationMenuItem[]>(() => [
  {
    label: 'Cursos',
    icon: 'i-lucide-book-open',
    to: '#',
    children: [
      {
        label: 'Huella hídrica',
        description: 'Descubre cómo calcular y reducir tu huella de agua.',
        icon: 'i-lucide-droplets',
        to: '/cursos'
      },
      {
        label: 'Reciclaje y residuos',
        description: 'Aprende sobre gestión de residuos y economía circular.',
        icon: 'i-lucide-recycle',
        to: '/cursos'
      },
      {
        label: 'Energías renovables',
        description: 'Explora fuentes limpias y sostenibles de energía.',
        icon: 'i-lucide-sun',
        to: '/cursos'
      },
      {
        label: 'Cambio climático',
        description: 'Entiende el impacto global y local del clima.',
        icon: 'i-lucide-cloud-sun',
        to: '/cursos'
      }
    ]
  },
  {
    label: 'Recursos',
    icon: 'i-lucide-folder-open',
    to: '#',
    children: [
      {
        label: 'Artículos',
        icon: 'i-lucide-file-text',
        description: 'Notas y artículos sobre sostenibilidad.',
        to: '#'
      },
      {
        label: 'Infografías',
        icon: 'i-lucide-image',
        description: 'Material visual educativo.',
        to: '#'
      },
      {
        label: 'Videos',
        icon: 'i-lucide-play-circle',
        description: 'Contenido audiovisual sobre temas ambientales.',
        to: '#'
      }
    ]
  },
  {
    label: 'Comunidad',
    icon: 'i-lucide-users',
    to: '#',
    children: [
      {
        label: 'Proyectos locales',
        icon: 'i-lucide-map-pin',
        description: 'Iniciativas sostenibles cerca de ti.',
        to: '#'
      },
      {
        label: 'Foro',
        icon: 'i-lucide-message-circle',
        description: 'Comparte ideas y soluciones ecológicas.',
        to: '#'
      }
    ]
  },
  {
    label: 'Sobre EcoUNI',
    icon: 'i-lucide-leaf',
    to: '#',
    children: [
      {
        label: 'Quiénes somos',
        icon: 'i-lucide-info',
        description: 'Conoce la historia y el propósito de EcoUNI.',
        to: '/sobre-nosotros'
      },
      {
        label: 'Contacto',
        icon: 'i-lucide-mail',
        description: 'Escríbenos o colabora con nosotros.',
        to: '/contacto'
      }
    ]
  }
])

function goAuth(){
  router.push("/auth")
}
</script>

<template>
  <UHeader mode="drawer">
    <template #title>
      <div class="flex items-center gap-2">
        <!-- <img src="/logo.png" alt="EcoUPA" class="h-6 w-6" /> -->
        <div class="flex items-center gap-2">
        <UIcon name="i-lucide-recycle" class="text-green-600 w-6 h-6" />
        <span class="font-semibold text-green-600">EcoUNI</span>
</div>

      </div>
    </template>

    <UNavigationMenu :items="items" />

    
    <template #right>
      <UButton  icon="i-lucide-user" size="lg" color="neutral" variant="link" @click="goAuth"/>
      <UColorModeButton />
    </template>
    <template #body>
      <UNavigationMenu :items="items" orientation="vertical" class="-mx-2.5 my-5" />
    </template>
  </UHeader>
</template>