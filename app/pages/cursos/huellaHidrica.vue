<script setup lang="ts">
const modules = [
  {
    title: "Módulo 1",
    subtitle: "¿Qué es la Huella Hídrica?",
    description: "Introducción clara para entender qué significa huella hídrica y por qué importa.",
    static: [
      "Definición explicada de forma sencilla"
    ],
    accordions: [
      {
        label: "Tipos de huella hídrica",
        content: [
          "Huella azul: agua superficial o subterránea",
          "Huella verde: agua de lluvia",
          "Huella gris: agua contaminada"
        ]
      },
      {
        label: "Ejemplos cotidianos",
        content: ["Ropa", "Alimentos", "Electricidad"]
      }
    ]
  },
  {
    title: "Módulo 2",
    subtitle: "¿Cuánta agua usamos sin saberlo?",
    description: "Descubre el impacto real del consumo diario y realiza un cálculo personal.",
    static: [
      "Actividad: Calcula tu huella hídrica personal"
    ],
    accordions: [
      {
        label: "Productos con alta huella hídrica",
        content: [
          "1 kg carne de res ≈ 15,000 L",
          "1 camiseta algodón ≈ 2,700 L",
          "1 taza de café ≈ 140 L"
        ]
      }
    ]
  },
  {
    title: "Módulo 3",
    subtitle: "¿Por qué importa?",
    description: "Entiende el impacto en el ambiente, la sociedad y el clima.",
    static: [
      "Escasez hídrica y sequías",
      "Impacto social por desigualdad",
      "Relación con el cambio climático"
    ],
    accordions: []
  },
  {
    title: "Módulo 4",
    subtitle: "Reducir mi huella hídrica",
    description: "Acciones en casa y consumo personal para reducir el impacto.",
    static: ["Actividad: Compromiso personal"],
    accordions: [
      {
        label: "Cambios en casa",
        content: [
          "Cerrar la llave al lavar dientes",
          "Reparar fugas",
          "Usar electrodomésticos eficientes"
        ]
      },
      {
        label: "Cambios en hábitos",
        content: [
          "Reducir carne un día por semana",
          "Comprar menos ropa",
          "Elegir productos sostenibles"
        ]
      }
    ]
  },
  {
    title: "Módulo 5",
    subtitle: "Actividades comunitarias",
    description: "Acciones colectivas para difundir y promover el cuidado del agua.",
    static: [
      "Mural o campaña",
      "Concurso de ideas sostenibles",
      "Feria o caminata del agua"
    ],
    accordions: []
  }
]
</script>

<template>
  <Navbar />

  <UContainer class="py-12">

    <div class="grid grid-cols-1 md:grid-cols-2 xl:grid-cols-3 gap-10">

      <UCard
        v-for="(m, i) in modules"
        :key="i"
        class="p-7 rounded-3xl border border-gray-200 dark:border-gray-800 bg-gray-50 dark:bg-gray-900 shadow-md"
      >

        <!-- Encabezado -->
        <div class="space-y-1 text-center">
          <h2 class="text-2xl font-bold text-gray-900 dark:text-gray-100">
            {{ m.title }}
          </h2>
          <p class="text-lg font-semibold text-primary-600 dark:text-primary-400">
            {{ m.subtitle }}
          </p>
        </div>

        <!-- Descripción -->
        <p class="mt-3 text-sm text-gray-600 dark:text-gray-400 text-center">
          {{ m.description }}
        </p>

        <!-- Línea sutil -->
        <div class="my-4 border-t border-gray-300 dark:border-gray-700"></div>

        <!-- Lista estática -->
        <ul class="space-y-2">
          <li
            v-for="item in m.static"
            :key="item"
            class="text-sm text-gray-700 dark:text-gray-300"
          >
            • {{ item }}
          </li>
        </ul>

        <!-- Acordeones -->
        <UAccordion
          v-if="m.accordions.length"
          class="mt-4"
          multiple
          :items="m.accordions.map(a => ({
            label: a.label,
            slot: a.label
          }))"
        />

        <!-- Contenido slotted -->
        <template v-for="a in m.accordions" :key="a.label" #[a.label]>
          <ul class="pl-4 pt-2 space-y-1 text-sm text-gray-600 dark:text-gray-400">
            <li v-for="c in a.content" :key="c">• {{ c }}</li>
          </ul>
        </template>

      </UCard>

    </div>

  </UContainer>

  <Footer />
</template>

