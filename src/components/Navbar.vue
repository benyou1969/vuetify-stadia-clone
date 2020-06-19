<template>
  <v-app-bar app color="white" flat class="px-12" hide-on-scroll>
    <div class="d-flex align-center">
      <router-link to="/">
        <v-img
          alt="stadia Logo"
          contain
          :src="smallLogo"
          transition="scale-transition"
          width="40"
      /></router-link>
      <v-img
        alt="stadia Name"
        class="shrink mt-1 hidden-sm-and-down"
        contain
        min-width="100"
        :src="logo"
        width="100"
        style="margin-left: -32px;"
      />
    </div>

    <v-spacer></v-spacer>

    <v-btn exact text :to="{ name: 'About' }">
      <span class="mr-2 text-none">About Stadia</span>
    </v-btn>
    <v-btn text :to="{ name: 'Games' }">
      <span class="mr-2 text-none">Games</span>
    </v-btn>
    <v-spacer class="hidden-sm-and-down"></v-spacer>

    <v-btn elevation text color="#de3334" class=" hidden-sm-and-down">
      <span class="mr-2 text-none  hidden-sm-and-down">Sign in</span>
    </v-btn>
    <v-btn class="btn-gradient  hidden-sm-and-down" depressed>
      <span class="mr-2 text-none white--text">Try now</span>
    </v-btn>
  </v-app-bar>
</template>

<script>
import Logo from "../assets/text-logo.svg";
import SmallLogo from "../assets/logo.svg";
export default {
  name: "Navbar",

  data: () => ({
    logo: Logo,
    smallLogo: SmallLogo
  })
};
</script>

<style>
.btn-gradient {
  background: rgb(248, 72, 29);
  background: linear-gradient(
    90deg,
    rgba(248, 72, 29, 1) 0%,
    rgba(220, 25, 95, 1) 100%,
    rgba(0, 212, 255, 1) 100%
  );
}
</style>
