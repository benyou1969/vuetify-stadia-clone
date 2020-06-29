<template>
  <v-app>
    <Appbar />
    <v-main> <router-view /></v-main>
    <Footer />
  </v-app>
</template>

<script>
import Appbar from "./components/Appbar";
import Footer from "./components/Footer";

export default {
  name: "App",

  components: {
    Appbar,
    Footer
  },

  data: () => ({
    //
  })
};
</script>

<style>
.v-btn--active {
  color: red !important;
}
</style>
