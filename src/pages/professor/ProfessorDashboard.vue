<template>
  <v-app>
    <!-- Header de la aplicación -->
    <Headers />

    <v-main>
      <v-container fluid>
        <v-row>
          <!-- Menú lateral del profesor -->
          <v-col cols="12" md="3" class="sidebar-container">
            <SidebarMenu />
          </v-col>

          <!-- Contenido principal del profesor -->
          <v-col cols="12" md="9" class="content-container">
            <Inicio />
          </v-col>
        </v-row>
      </v-container>
    </v-main>
  </v-app>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import Headers from '@/components/professor/Headers.vue'
import SidebarMenu from '@/components/professor/SidebarMenu.vue'
import Inicio from '@/components/professor/Inicio.vue'

export default defineComponent({
  name: 'ProfessorDashboard',
  components: {
    Headers,
    SidebarMenu,
    Inicio,
  }
})
</script>

<style scoped src="@/styles/professor/ProfessorDashboard.scss"></style>
