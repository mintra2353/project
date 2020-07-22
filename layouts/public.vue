<template>
    <v-app>
    <v-system-bar dark color="red lighten-2">
      <v-icon>mdi-signal-cellular-outline</v-icon>
      <v-icon>mdi-wifi-strength-4</v-icon>
      <v-spacer></v-spacer>
      <v-icon>mdi-battery</v-icon>
      <span>12:30</span>
    </v-system-bar>
      <v-main>
    <v-content>
        <nuxt/>
    </v-content>
  </v-main>
    <v-footer
    color="primary lighten-1"
    padless
  >
    <v-row
      justify="center"
      no-gutters
    >
      <v-col
        class="red lighten-2 py-4 text-center white--text"
        cols="12"
      >
        {{ new Date().getFullYear() }} — <strong>Vuetify</strong>
      </v-col>
    </v-row>
  </v-footer>
  </v-app>
</template>