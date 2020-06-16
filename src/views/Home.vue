<template>
  <div class="home">
    <v-card color="#202124" class="white--text pa-2">
      <v-row>
        <v-col cols="6">
          <v-card outlined tile color="#202124" class="white--text pa-8">
            <v-card-text>
              <div class="grey--text text--lighten-2 text-h3">Play on us</div>
              <div class="grey--text text--lighten-1 my-5 text-h6">
                Get instant access to a collection of games with a 1 month
                Stadia Pro trial
              </div>
              <v-btn class="btn-gradient" depressed x-large>
                <span class="mr-2 text-none white--text">Try now</span>
              </v-btn>
              <p class="grey--text text--lighten-1 my-5">
                $9.99/mo after trial, cancel anytime.
              </p>
            </v-card-text>
          </v-card>
        </v-col>
        <v-col cols="6">
          <v-card outlined tile color="#202124" class="white--text pa-2">
            .col-6
          </v-card>
        </v-col>
      </v-row>
    </v-card>
  </div>
</template>

<script>
// @ is an alias to /src

export default {
  name: "Home"
};
</script>
