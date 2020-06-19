<template>
  <div>
    <div class="d-flex justify-center my-8">
      <v-img :src="logoPro" max-width="300"></v-img>
    </div>
    <div class="text-center text-h4 my-8">
      Build a library of incredible games with Stadia Pro
    </div>
    <div class="text-center text-h5 my-4 grey--text text--darken-1">
      Claim games for your collection every month.
    </div>
    <br />
    <div>
      <v-row align="center" justify="center">
        <v-col
          cols="4"
          sm="4"
          md="3"
          lg="2"
          v-for="image in images"
          :key="image.title"
        >
          <v-card class="mx-auto" outlined color="transparent">
            <v-img :src="image.src" height="279px"></v-img>
            <div class="text-center text--caption">{{ image.title }}</div>
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
    <div>
      <v-row align="center" justify="center">
        <v-col
          cols="4"
          sm="4"
          md="2"
          lg="2"
          v-for="image in otherImages"
          :key="image.title"
        >
          <v-card class="mx-auto" outlined color="transparent">
            <v-img :src="image.src" height="200px"></v-img>
            <div class="text-center">{{ image.title }}</div>
          </v-card>
        </v-col>
      </v-row>
    </div>
    <br />
  </div>
</template>

<script>
import LogoPro from "@/assets/logo-pro.svg";

export default {
  name: "Games",
  data: () => ({
    logoPro: LogoPro,
    images: [
      {
        src:
          "https://www.gstatic.com/stadia/gamers/landing_page/assets/games/Octopath_Traveler.png",
        title: "Get Packed"
      },
      {
        src:
          "https://www.gstatic.com/stadia/gamers/landing_page/assets/games/Serious_Sam_Collection.png",
        title: "Serious Sam Collection"
      },
      {
        src:
          "https://www.gstatic.com/stadia/gamers/landing_page/assets/games/PlayerUnknown_s_Battlegrounds.png",
        title: "PlayerUnknown's Battlegrounds"
      },
      {
        src:
          "https://www.gstatic.com/stadia/gamers/landing_page/assets/games/SteamWorld_Quest__Hand_of_Gilgamech.png",
        title: "SteamWorld Quest: Hand of Gilgamech"
      },
      {
        src:
          "https://www.gstatic.com/stadia/gamers/landing_page/assets/games/Little_Nightmares.png",
        title: "Little Nightmares"
      },
      {
        src:
          "https://www.gstatic.com/stadia/gamers/landing_page/assets/games/SteamWorld_Heist.png",
        title: "SteamWorld Heist"
      },
      {
        src:
          "https://www.gstatic.com/stadia/gamers/landing_page/assets/games/spitlings.png",
        title: "Spitlings"
      },
      {
        src:
          "https://www.gstatic.com/stadia/gamers/landing_page/assets/games/SUPERHOT.png",
        title: "SUPERHOT"
      },
      {
        src:
          "https://www.gstatic.com/stadia/gamers/landing_page/assets/games/Panzer_Dragoon_Remake.png",
        title: "Panzer Dragoon"
      },
      {
        src:
          "https://www.gstatic.com/stadia/gamers/landing_page/assets/games/Zombie_Army_4__Dead_War.png",
        title: "Zombie Army 4: Dead War"
      },
      {
        src:
          "https://www.gstatic.com/stadia/gamers/landing_page/assets/games/gylt.png",
        title: "GYLT"
      },
      {
        src:
          "https://www.gstatic.com/stadia/gamers/landing_page/assets/games/Stacks_on_Stacks__On_Stacks_.png",
        title: "Stacks on Stacks (On Stacks)"
      },
      {
        src:
          "https://www.gstatic.com/stadia/gamers/landing_page/assets/games/SteamWorld_Dig_2.png",
        title: "SteamWorld Dig 2"
      },
      {
        src:
          "https://www.gstatic.com/stadia/gamers/landing_page/assets/games/GRID.png",
        title: "GRID"
      },
      {
        src:
          "https://www.gstatic.com/stadia/gamers/landing_page/assets/games/The_Turing_Test.png",
        title: "The Turing Test"
      },
      {
        src:
          "https://www.gstatic.com/stadia/gamers/landing_page/assets/games/Destiny_2__The_Collection.png",
        title: "Destiny 2: The Collection"
      },
      {
        src:
          "https://www.gstatic.com/stadia/gamers/landing_page/assets/games/Power_Rangers__Battle_for_the_Grid.png",
        title: "Power Rangers: Battle for the Grid"
      }
    ],
    otherImages: [
      {
        src:
          "https://www.gstatic.com/stadia/gamers/landing_page/assets/games/Tomb_Raider__Definitive_Edition.png",
        title: "Tomb Raider: Definitive Edition"
      },
      {
        src:
          "https://www.gstatic.com/stadia/gamers/landing_page/assets/games/NBA2k20.png",
        title: "NBA 2K20"
      },
      {
        src:
          "https://www.gstatic.com/stadia/gamers/landing_page/assets/games/MotoGP20.png",
        title: "MotoGP(TM) 20"
      },
      {
        src:
          "https://www.gstatic.com/stadia/gamers/landing_page/assets/games/Tom_Clancy_s_The_Division_2.png",
        title: "Tom Clancy's The Division 2"
      },
      {
        src:
          "https://www.gstatic.com/stadia/gamers/landing_page/assets/games/SAMURAI_SHODOWN.png",
        title: "Samurai Shodown"
      },
      {
        src:
          "https://www.gstatic.com/stadia/gamers/landing_page/assets/games/Steamworld_Dig.png",
        title: "Steamworld Dig"
      },
      {
        src:
          "https://www.gstatic.com/stadia/gamers/landing_page/assets/games/Monopoly.png",
        title: "Monopoly"
      },
      {
        src:
          "https://www.gstatic.com/stadia/gamers/landing_page/assets/games/FootballManager2020.png",
        title: "Football Manager 2020"
      },
      {
        src:
          "https://www.gstatic.com/stadia/gamers/landing_page/assets/games/Mortal_Kombat_11.png",
        title: "Mortal Kombat 11"
      },
      {
        src:
          "https://www.gstatic.com/stadia/gamers/landing_page/assets/games/JustDance2020.png",
        title: "Just Dance 2020"
      },
      {
        src:
          "https://www.gstatic.com/stadia/gamers/landing_page/assets/games/Kine.png",
        title: "Kine"
      },
      {
        src:
          "https://www.gstatic.com/stadia/gamers/landing_page/assets/games/Metro_Exodus.png",
        title: "Metro Exodus"
      },
      {
        src:
          "https://www.gstatic.com/stadia/gamers/landing_page/assets/games/Supercross_3.png",
        title: "Supercross 3"
      },
      {
        src:
          "https://www.gstatic.com/stadia/gamers/landing_page/assets/games/Borderlands3.png",
        title: "Borderlands 3"
      },
      {
        src:
          "https://www.gstatic.com/stadia/gamers/landing_page/assets/games/FarmingSimulator19.png",
        title: "Farming Simulator 19"
      },
      {
        src:
          "https://www.gstatic.com/stadia/gamers/landing_page/assets/games/Shadow_of_the_Tomb_Raider__Definitive_Edition.png",
        title: "Kine"
      },
      {
        src:
          "https://www.gstatic.com/stadia/gamers/landing_page/assets/games/Rage_2.png",
        title: "Rage 2"
      },
      {
        src:
          "https://www.gstatic.com/stadia/gamers/landing_page/assets/games/Red_Dead_Redemption_2.png",
        title: "Red Dead Redemption 2"
      },
      {
        src:
          "https://www.gstatic.com/stadia/gamers/landing_page/assets/games/GhostReconBreakPoint.png",
        title: "Ghost Recon Breakpoint"
      },
      {
        src:
          "https://www.gstatic.com/stadia/gamers/landing_page/assets/games/DarskidersGenesis.png",
        title: "Darksiders Genesis"
      },
      {
        src:
          "https://www.gstatic.com/stadia/gamers/landing_page/assets/games/Octopath_Traveler.png",
        title: "Octopath Traveler"
      },
      {
        src:
          "https://www.gstatic.com/stadia/gamers/landing_page/assets/games/Wolfenstein__Youngblood.png",
        title: "Wolfenstein Young Blood"
      }
    ]
  })
};
</script>

<style scoped>
.v-image {
  border-radius: 8px;
}
</style>
