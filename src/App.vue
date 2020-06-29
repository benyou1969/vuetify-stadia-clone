<template>
  <v-app>
    <Appbar />
    <v-main>
      <transition name="slide" mode="out-in">
        <router-view />
      </transition>
    </v-main>
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

.slide-enter {
  transform: translateY(100px);
  opacity: 0;
}

.slide-enter-active,
.slide-leave-active {
  transition: all 0.5s ease-out;
}

.slide-leave {
  transform: translateY(-100px);
  opacity: 0;
}
</style>
