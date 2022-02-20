<template>
  <v-app style="background:#c5eff7;">

<v-main>
    <Nuxt/>
</v-main>

    <v-footer
     color="#c5eff7"
    padless

    >
        <v-col
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