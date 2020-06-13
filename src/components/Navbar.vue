<template>
  <v-app-bar app color="primary" dark>
    <div class="d-flex align-center">
      <v-img
        alt="stadia Logo"
        class="shrink mr-2"
        contain
        src="https://cdn.vuetifyjs.com/images/logos/vuetify-logo-dark.png"
        transition="scale-transition"
        width="40"
      />

      <v-img
        alt="stadia Name"
        class="shrink mt-1 hidden-sm-and-down"
        contain
        min-width="100"
        :src="logo"
        width="100"
      />
    </div>

    <v-spacer></v-spacer>

    <v-btn
      href="https://github.com/vuetifyjs/vuetify/releases/latest"
      target="_blank"
      text
    >
      <span class="mr-2">Latest Release</span>
      <v-icon>mdi-open-in-new</v-icon>
    </v-btn>
  </v-app-bar>
</template>

<script>
import Logo from '../assets/logo.svg'
export default {
  name: "Navbar",

  data: () => ({
    logo: Logo
  })
};
</script>
