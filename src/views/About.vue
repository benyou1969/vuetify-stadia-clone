<template>
  <div class="home">
    <v-card color="#202124" class="my-1 my-sm-2 my-md-4 mx-4 mx-sm-8 mx-md-16">
      <v-row align="center" justify="center">
        <v-col cols="12" sm="12" md="6">
          <v-card outlined tile color="#202124" class="white--text pa-md-8">
            <v-card-text>
              <div class="grey--text text--lighten-2 text-h3 text-sm-4">
                Play on us
              </div>
              <div class="grey--text text--lighten-1 my-5 text-h6">
                Get instant access to a collection of games with a 1 month
                Stadia Pro trial
              </div>
              <v-btn
                class="btn-gradient"
                depressed
                x-large
                :block="$vuetify.breakpoint.mobile"
              >
                <span class="mr-2 text-none white--text">Try now</span>
              </v-btn>
              <p class="grey--text text--lighten-1 my-5">
                $9.99/mo after trial, cancel anytime.
              </p>
            </v-card-text>
          </v-card>
        </v-col>
        <v-col sm="11" md="6">
          <v-card color="#202124" flat>
            <v-img
              src="https://www.gstatic.com/stadia/gamers/landing_page/assets/pro_hero_h_2x.png"
              lazy-src="https://www.gstatic.com/stadia/gamers/landing_page/assets/pro_hero_h_2x.png"
            ></v-img>
          </v-card>
        </v-col>
      </v-row>
    </v-card>

    <div
      class="grey--text text--darken-4 font-weight-regular text-lg-h2 text-md-h3  text-center mt-10 text-h4"
    >
      Get even more games
    </div>

    <div
      class="font-weight-regular text-lg-h4 text-md-h5 text-sm-h6 text-center my-4 red--text text--lighten-1"
    >
      Get $10 off your first game purchase in the Stadia store with Pro.
    </div>

    <div class="my-1 my-sm-2 my-md-4 mx-4 mx-sm-8 mx-md-16">
      <v-card color="transparent" flat>
        <v-row align="center" justify="center">
          <v-col
            cols="4"
            sm="4"
            md="2"
            lg="2"
            v-for="image in images"
            :key="image"
          >
            <v-card class="mx-auto">
              <v-img :src="image" :lazy-src="image" height="200px"></v-img>
            </v-card>
          </v-col>
        </v-row>
      </v-card>
    </div>
    <div class="text-center">
      <v-btn text x-large :to="{ name: 'Games' }" :ripple="false">
        <span class="mr-2 text-none red--text">See All Games</span>
      </v-btn>
    </div>

    <br />

    <v-card color="transparent" flat class="pa-2">
      <v-row>
        <v-col cols="12" sm="12" md="6">
          <v-card flat class="pa-md-2">
            <v-img
              lazy-src="https://www.gstatic.com/stadia/gamers/landing_page/assets/play_anywhere@2x.jpg"
              src="https://www.gstatic.com/stadia/gamers/landing_page/assets/play_anywhere@2x.jpg"
            ></v-img>
          </v-card>
        </v-col>
        <v-col>
          <v-card flat class=" pa-md-8">
            <v-card-text>
              <div class="grey--text text--darken-4 text-h3">
                Play instantly across your devices
              </div>
              <div class="grey--text text--darken-1 my-5 text-body-1">
                Play instantly with one click You choose the screens where your
                games live. Play on
                <a
                  class="red--text text-decoration-none"
                  href="https://support.google.com/stadia/answer/9578631"
                  target="_blank"
                  >compatible</a
                >
                laptops, desktops, phones, and tablets. It’s up to you. And to
                play on TVs, grab
                <a
                  hre="https://store.google.com/regionpicker"
                  class="red--text text-decoration-none"
                  >Stadia Premiere Edition</a
                >, available now on the Google Store.
              </div>
            </v-card-text>
          </v-card>
        </v-col>
      </v-row>
    </v-card>

    <br />
    <v-card color="rgb(248, 248, 249)" flat v-intersect="showMoreContent">
      <v-row align="end" justify="end" v-if="loadNewContent">
        <v-col cols="12" sm="12" md="6">
          <v-card flat class="pa-8" color="rgb(248, 248, 249)">
            <v-card-text>
              <div class="grey--text text--darken-4 text-h3">
                The Stadia platform is free to join
              </div>
              <div class="grey--text text--darken-1 my-5 text-body-1">
                You don’t need special hardware or an invitation to play, just
                the screens and controllers you already have. You can purchase a
                variety of great games on the Stadia store and play them through
                Wi-Fi and wired internet connections.
              </div>
            </v-card-text>
          </v-card>
        </v-col>
        <v-col cols="12" sm="12" md="6">
          <v-card flat color="rgb(248, 248, 249)">
            <v-img
              src="https://www.gstatic.com/stadia/gamers/landing_page/assets/beacon_hero.png"
              lazy-src="https://www.gstatic.com/stadia/gamers/landing_page/assets/beacon_hero.png"
            ></v-img>
          </v-card>
        </v-col>
      </v-row>
    </v-card>
    <br />
    <br />
    <v-card flat class="my-1 my-sm-2 my-md-4 mx-4 mx-sm-8 mx-md-16">
      <v-row>
        <v-col cols="12" sm="6" md="6">
          <v-card flat class=" pa-md-8">
            <v-card-text>
              <div class="grey--text text--darken-4 text-h4 text-md-h3">
                Claim games for free with Stadia Pro
              </div>
              <div class="grey--text text--darken-1 text-body-1 my-5">
                You can get free games with Stadia Pro. Games are available the
                moment you subscribe, and every month you stay subscribed you
                get more free games.
              </div>
            </v-card-text>
          </v-card>
        </v-col>

        <v-col cols="12" sm="6">
          <v-card flat class="pa-2">
            <v-img
              :src="logoPro"
              :lazy-src="logoPro"
              class="mb-8"
              max-width="300"
            ></v-img>
            <div class="my-2 text-subtitle-1 grey--text text--darken-4">
              <v-icon color="red">mdi-check</v-icon> Access to free games
              instantly, with more added every month
            </div>
            <div class="my-2 text-subtitle-1 grey--text text--darken-4">
              <v-icon color="red">mdi-check</v-icon> Exclusive discounts
            </div>
            <div class="my-2 text-subtitle-1 grey--text text--darken-4">
              <v-icon color="red">mdi-check</v-icon> Play in up to 4K HDR with
              5.1 surround sound
            </div>
            See
            <a
              href="https://support.google.com/stadia"
              class="red--text text-decoration-none"
              >support.google.com/stadia</a
            >
            for details.
          </v-card>
        </v-col>
      </v-row>
    </v-card>
    <br />
  </div>
</template>

<script>
// @ is an alias to /src
import LogoPro from "@/assets/logo-pro.svg";

export default {
  name: "About",
  data: () => ({
    loadNewContent: false,
    logoPro: LogoPro,
    images: [
      "https://www.gstatic.com/stadia/gamers/landing_page/assets/games/Octopath_Traveler.png",
      "https://www.gstatic.com/stadia/gamers/landing_page/assets/games/NBA2k20.png",
      "https://www.gstatic.com/stadia/gamers/landing_page/assets/games/Red_Dead_Redemption_2.png",
      "https://www.gstatic.com/stadia/gamers/landing_page/assets/games/Mortal_Kombat_11.png",
      "https://www.gstatic.com/stadia/gamers/landing_page/assets/games/DoomEternal.png"
    ]
  }),
  methods: {
    showMoreContent(entries) {
      console.log(entries);
      this.loadNewContent = entries[0].isIntersecting;
    }
  }
};
</script>
