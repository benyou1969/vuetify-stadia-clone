<template>
  <div class="my-1 my-sm-2 my-md-4 mx-4 mx-sm-8 mx-md-16">
    <div class="d-flex justify-center my-8">
      <v-img :src="logoPro" :lazy-src="logoPro" max-width="300"></v-img>
    </div>
    <div class="text-center text-h4 my-8">
      Build a library of incredible games with Stadia Pro
    </div>
    <div class="text-center text-h5 my-4 grey--text text--darken-1">
      Claim games for your collection every month.
    </div>
    <br />
    <div>
      <v-row align="start" justify="start">
        <v-col
          cols="4"
          sm="4"
          md="3"
          lg="2"
          v-for="image in images"
          :key="image.title"
        >
          <v-card class="mx-auto" outlined color="transparent">
            <v-img
              :src="image.src"
              :lazy-src="image.src"
              :height="$vuetify.breakpoint.smAndDown ? `180` : `300px`"
            ></v-img>
            <div class="text-center grey--text text--darken-1 my-2">
              {{ image.title }}
            </div>
          </v-card>
        </v-col>
      </v-row>
    </div>
    <br />
    <div class="text-center text-h4 my-8">
      Buy more of your favorites in the Stadia store
    </div>
    <div class="text-center text-h6 my-4 grey--text text--darken-1">
      Purchase new games and play them instantly across
      <a
        class="red--text text-decoration-none"
        href="https://support.google.com/stadia/answer/9578631"
        >compatible</a
      >
      devices, with no waiting for downloads or in-game updates
    </div>
    <div v-intersect="showMoreContent">
      <v-row align="start" justify="start" v-if="loadNewContent">
        <v-col
          cols="4"
          sm="4"
          md="3"
          lg="2"
          v-for="image in otherImages"
          :key="image.title"
        >
          <v-card class="mx-auto" outlined color="transparent">
            <v-img
              :src="image.src"
              :lazy-src="image.src"
              :height="$vuetify.breakpoint.smAndDown ? `180` : `300`"
            ></v-img>
            <div class="text-center grey--text text--darken-1 my-2">
              {{ image.title }}
            </div>
          </v-card>
        </v-col>
      </v-row>
    </div>
    <br />
  </div>
</template>

<script>
import LogoPro from "@/assets/logo-pro.svg";
import Image1 from "../assets/images/Octopath_Traveler-1.png";
import Image2 from "../assets/images/images/Serious_Sam_Collection.png";
import Image3 from "../assets/images/images/PlayerUnknown_s_Battlegrounds.png";
import Image18 from "../assets/images/images/SteamWorld_Dig_2.png";
import Image5 from "../assets/images/images/Little_Nightmares.png";
import Image6 from "../assets/images/images/SteamWorld_Heist.png";
import Image7 from "../assets/images/images/spitlings.png";
import Image10 from "../assets/images/images/Zombie_Army_4__Dead_War.png";
import Image9 from "../assets/images/images/gylt.png";
import Image8 from "../assets/images/images/Stacks_on_Stacks__On_Stacks_.png";
import Image4 from "../assets/images/images/SteamWorld_Quest__Hand_of_Gilgamech.png";
import Image12 from "../assets/images/images/GRID.png";
import Image13 from "../assets/images/images/The_Turing_Test.png";
import Image14 from "../assets/images/images/Destiny_2__The_Collection.png";
import Image15 from "../assets/images/images/Power_Rangers__Battle_for_the_Grid.png";
import Image16 from "../assets/images/images/SUPERHOT.png";
import Image17 from "../assets/images/images/Panzer_Dragoon_Remake.png";

import OtherImage1 from "../assets/images/NBA2k20.png";
import OtherImage2 from "../assets/images/otherImages/Shadow_of_the_Tomb_Raider__Definitive_Edition.png";
import OtherImage3 from "../assets/images/otherImages/MotoGP20.png";
import OtherImage4 from "../assets/images/otherImages/Tom_Clancy_s_The_Division_2.png";
import OtherImage5 from "../assets/images/otherImages/SAMURAI_SHODOWN.png";
import OtherImage6 from "../assets/images/otherImages/Steamworld_Dig.png";
import OtherImage7 from "../assets/images/otherImages/Monopoly.png";
import OtherImage8 from "../assets/images/otherImages/FootballManager2020.png";
import OtherImage9 from "../assets/images/otherImages/Mortal_Kombat_11.png";
import OtherImage10 from "../assets/images/otherImages/JustDance2020.png";
import OtherImage11 from "../assets/images/otherImages/Metro_Exodus.png";
import OtherImage12 from "../assets/images/otherImages/Supercross_3.png";
import OtherImage13 from "../assets/images/otherImages/Borderlands3.png";
import OtherImage14 from "../assets/images/otherImages/FarmingSimulator19.png";
import OtherImage15 from "../assets/images/otherImages/Rage_2.png";

import OtherImages16 from "../assets/images/Red_Dead_Redemption_2.png";
import OtherImages17 from "../assets/images/otherImages/GhostReconBreakPoint.png";
import OtherImages18 from "../assets/images/otherImages/DarskidersGenesis.png";
import OtherImages20 from "../assets/images/otherImages/Wolfenstein__Youngblood.png";
// import OtherImages3 from "../assets/images/Mortal_Kombat_11.png";
// import OtherImages4 from "../assets/images/DoomEternal.png";

export default {
  name: "Games",
  data: () => ({
    loadNewContent: false,
    logoPro: LogoPro,
    images: [
      {
        src: Image1,
        title: "Get Packed"
      },
      {
        src: Image2,
        title: "Serious Sam Collection"
      },
      {
        src: Image3,
        title: "PlayerUnknown's Battlegrounds"
      },
      {
        src: Image4,
        title: "SteamWorld Quest: Hand of Gilgamech"
      },
      {
        src: Image5,
        title: "Little Nightmares"
      },
      {
        src: Image6,
        title: "SteamWorld Heist"
      },
      {
        src: Image7,
        title: "Spitlings"
      },
      {
        src: Image16,
        title: "SUPERHOT"
      },
      {
        src: Image17,
        title: "Panzer Dragoon"
      },
      {
        src: Image10,
        title: "Zombie Army 4: Dead War"
      },
      {
        src: Image9,
        title: "GYLT"
      },
      {
        src: Image8,
        title: "Stacks on Stacks (On Stacks)"
      },
      {
        src: Image18,
        title: "SteamWorld Dig 2"
      },
      {
        src: Image12,
        title: "GRID"
      },
      {
        src: Image13,
        title: "The Turing Test"
      },
      {
        src: Image14,
        title: "Destiny 2: The Collection"
      },
      {
        src: Image15,
        title: "Power Rangers: Battle for the Grid"
      }
    ],
    otherImages: [
      {
        src: OtherImage2,
        title: "Tomb Raider: Definitive Edition"
      },
      {
        src: OtherImage1,
        title: "NBA 2K20"
      },
      {
        src: OtherImage3,
        title: "MotoGP(TM) 20"
      },
      {
        src: OtherImage4,
        title: "Tom Clancy's The Division 2"
      },
      {
        src: OtherImage5,
        title: "Samurai Shodown"
      },
      {
        src: OtherImage6,
        title: "Steamworld Dig"
      },
      {
        src: OtherImage7,
        title: "Monopoly"
      },
      {
        src: OtherImage8,
        title: "Football Manager 2020"
      },
      {
        src: OtherImage9,
        title: "Mortal Kombat 11"
      },
      {
        src: OtherImage10,
        title: "Just Dance 2020"
      },
      {
        src: OtherImage11,
        title: "Metro Exodus"
      },
      {
        src: OtherImage12,
        title: "Supercross 3"
      },
      {
        src: OtherImage13,
        title: "Borderlands 3"
      },
      {
        src: OtherImage14,
        title: "Farming Simulator 19"
      },
      {
        src: Image2,
        title: "Kine"
      },
      {
        src: OtherImage15,
        title: "Rage 2"
      },
      {
        src: OtherImages16,
        title: "Red Dead Redemption 2"
      },
      {
        src: OtherImages17,
        title: "Ghost Recon Breakpoint"
      },
      {
        src: OtherImages18,
        title: "Darksiders Genesis"
      },
      {
        src: Image1,
        title: "Octopath Traveler"
      },
      {
        src: OtherImages20,
        title: "Wolfenstein Young Blood"
      }
    ]
  }),
  methods: {
    showMoreContent(entries) {
      console.log(entries[0].isIntersecting);
      this.loadNewContent = entries[0].isIntersecting;
    }
  }
};
</script>

<style scoped>
.v-image {
  border-radius: 8px;
}
</style>
