<template>
  <v-app>
    <v-main>
      <v-container>
        <Nuxt />
      </v-container>
    </v-main>
    <v-footer
     color="#c5eff7"
    padless
    >
        <v-col
        color="primary lighten-1"
        class=" text-center"
        cols="12">
          {{ new Date().getFullYear() }} — <strong>Bluwm</strong>
        </v-col>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  name: 'DefaultLayout',
  data() {
    return {
     
    }
  },
}
</script>
