<script setup lang="ts">
const form = reactive({
  email: "",
  name: "",
  message: ""
})

const toast = useToast()

function showToast() {
  toast.add({
    title: "Mensaje enviado",
    description: "Gracias por contactarnos. Responderemos pronto.",
    icon: "i-lucide-check-circle",
    
  })
  form.email = ""
  form.name = ""
  form.message = ""
}
</script>

<template>
  <Navbar />

  <UMain class="py-16 px-4">
    <div class="max-w-3xl mx-auto space-y-10">

      <!-- TITULO -->
      <section class="text-center space-y-3">
        <h1 class="text-5xl font-extrabold">Contacto</h1>
        <p class="text-lg text-gray-600 dark:text-gray-300">
          Si tienes dudas, propuestas o quieres colaborar con EcoUNI, llena este formulario.
        </p>
      </section>

      <!-- FORMULARIO -->
      <UCard class="p-6 rounded-2xl">

        <UForm :state="form" class="space-y-4">

          <!-- EMAIL -->
          <UFormField
            label="Correo electrónico"
            description="No compartiremos tu correo con nadie."
            help="Ingresa un correo válido."
            size="xl"
          >
            <UInput
              v-model="form.email"
              placeholder="tucorreo@example.com"
              type="email"
              class="w-full"
            />
          </UFormField>

          <!-- NOMBRE -->
          <UFormField
            label="Nombre"
            description="Cómo quieres que nos refiramos a ti."
            size="xl"
          >
            <UInput
              v-model="form.name"
              placeholder="Tu nombre"
              class="w-full"
            />
          </UFormField>

          <!-- MENSAJE -->
          <UFormField
            label="Mensaje"
            description="Cuéntanos qué necesitas."
            size="xl"
          >
            <UTextarea
              v-model="form.message"
              placeholder="Escribe tu mensaje aquí..."
              class="w-full h-40"
            />
          </UFormField>

          <!-- BOTÓN -->
          <div class="pt-4 flex justify-end">
            <UButton
              size="xl"
              color="primary"
              icon="i-lucide-send"
              @click="showToast"
            >
              Enviar mensaje
            </UButton  >
          </div>

        </UForm>

      </UCard>
    </div>
  </UMain>

  <Footer />
</template>
