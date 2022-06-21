<template>
  <v-container fluid color="grey lighten-4" class="ma-0 pa-0">
    <div style="position: relative;">
      <v-carousel hide-delimiters next-icon prev-icon>
        <v-carousel-item v-for="n in slideImage" :key="n" :src="n" reverse-transition="fade-transition"
          transition="fade-transition">
          <v-row class="fill-height" justify="center">
            <v-col class="fill-width" align="center" justify="center">
              <div class="h5 title pt-14">
                私たちが経験した平凡な日常は、連続して起こる奇跡かもしれません
              </div>
              <div class="h5 title">
                The mundane everyday we have experienced may be a series of
                miracles
              </div>
            </v-col>
          </v-row>
        </v-carousel-item>
      </v-carousel>
    </div>
    <div style="position:relative;margin-top:-150px;">
      <card />
    </div>
    <div class="pa-10">
      <v-alert class="font-italic" border="left" colored-border color="white" elevation="2" style="text-align: center">
        I'am a Back end Development and I like travel! <br />
        The origin of this blog is also limited to my desire to test my
        abilities and record my own life.
      </v-alert>
    </div>
    <div class="px-15">
      <v-row>
        <v-col v-for="n in 3" :key="n" class="d-flex child-flex" cols="4">
          <v-img :src="`https://picsum.photos/500/300?image=${n * 5 + 10}`"
            :lazy-src="`https://picsum.photos/10/6?image=${n * 5 + 10}`" aspect-ratio="1" class="grey lighten-2">
            <template v-slot:placeholder>
              <v-row class="fill-height ma-0" align="center" justify="center">
                <v-progress-circular indeterminate color="grey lighten-5"></v-progress-circular>
              </v-row>
            </template>
            <v-fade-transition>
              <v-overlay absolute color="#036358">
                <v-btn>See more info</v-btn>
              </v-overlay>
            </v-fade-transition>
          </v-img>
        </v-col>
      </v-row>
    </div>
  </v-container>
</template>

<script>
import card from "./Card.vue";

import colors from "vuetify/lib/util/colors";

export default {
  components: {
    card,
  },
  data() {
    return {
      slideImage: [require("@/assets/bg.jpg")],
      color: {
        white: colors.white,
      },
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/scss/main.scss";
</style>
