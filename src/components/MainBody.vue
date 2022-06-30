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
              <div class="title">
                The mundane everyday we have experienced may be a series of
                miracles
              </div>
              <div class="title">
                我們所經歷的每個平凡的日常，也許就是連續發生的奇蹟。
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
      <about />
    </div>
    <div class="pb-10 pt-5 subTitle">
      <skills />
    </div>
    <div class="pb-10 pt-5 subTitle">
      <timeLine />
    </div>
    <div class="pb-10 pt-10 subTitle">
      <portfolio />
    </div>
  </v-container>
</template>

<script>
import card from "./Card.vue";
import skills from "./Skills.vue"
import timeLine from "./TimeLine.vue"
import about from "./AboutMe.vue"
import portfolio from "./Portfolio.vue"

import colors from "vuetify/lib/util/colors";

export default {
  components: {
    about,
    card,
    skills,
    timeLine,
    portfolio
  },

  data() {

    return {
      slideImage: [require("@/assets/bg.jpg")],
      color: {
        white: colors.white,
      },
      show: false,
    };
  },

};
</script>

<style lang="scss" scoped>
@import "../assets/scss/main.scss";
</style>
