<template>
  <v-app style="margin: 1rem 4rem;">
    <Navbar />
    <v-content> <router-view /></v-content>
    <Footer />
  </v-app>
</template>

<script>
import Navbar from "./components/Navbar";
import Footer from "./components/Footer";

export default {
  name: "App",

  components: {
    Navbar,
    Footer
  },

  data: () => ({
    //
  })
};
</script>
