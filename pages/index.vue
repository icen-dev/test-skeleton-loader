<template>
  <v-layout column justify-center align-center>
    <v-flex xs12 sm8 md6>
      <v-btn @click="loading = !loading">test</v-btn>
      <p>Loading: {{ loading }}</p>
      <v-card width="100vw">
        <v-skeleton-loader v-if="!loading" max-width="100%" type="image" />
        <v-img v-if="loading" :src="require('~/assets/sample.jpg')" />
        <v-card-title class="headline">
          Welcome to the Vuetify + Nuxt.js template
        </v-card-title>
        <v-card-text>
          <p>
            Vuetify is a progressive Material Design component framework for
            Vue.js. It was designed to empower developers to create amazing
            applications.
          </p>
        </v-card-text>
      </v-card>
    </v-flex>
  </v-layout>
</template>

<script>
export default {
  components: {},
  data: () => ({
    loading: false
  })
}
</script>
