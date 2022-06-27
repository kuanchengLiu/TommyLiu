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
      <v-alert class="font-italic" border="left" colored-border color="white" elevation="2" style="text-align: center">
        I'am a Back end Development and I like travel! <br />
        The origin of this blog is also limited to my desire to test my
        abilities and record my own life.
      </v-alert>
    </div>
    <div class="pb-10 pt-5 subTitle">
      <skills />
    </div>
    <div class="pb-10 pt-5 subTitle">
      <timeLine />
    </div>
    <div class="pb-10 pt-10 subTitle">
      PORTFOLIO
    </div>
    <div>
      <v-card class="mx-auto" max-width="344">
        <v-img src="https://cdn.vuetifyjs.com/images/cards/sunshine.jpg" height="200px"></v-img>
        <v-card-title>
          Top western road trips
        </v-card-title>
        <v-card-subtitle>
          1,000 miles of wonder
        </v-card-subtitle>

        <v-card-actions>
          <v-btn color="orange lighten-2" text>
            Explore
          </v-btn>

          <v-spacer></v-spacer>

          <v-btn icon @click="show = !show">
            <v-icon>{{ show ? 'mdi-chevron-up' : 'mdi-chevron-down' }}</v-icon>
          </v-btn>
        </v-card-actions>

        <v-expand-transition>
          <div v-show="show">
            <v-divider></v-divider>

            <v-card-text>
              I'm a thing. But, like most politicians, he promised more than he could deliver. You won't have time for
              sleeping, soldier, not with all the bed making you'll be doing. Then we'll go with that data file! Hey,
              you add a one and two zeros to that or we walk! You're going to do his laundry? I've got to find a way to
              escape.
            </v-card-text>
          </div>
        </v-expand-transition>
      </v-card>
    </div>
  </v-container>
</template>

<script>
import card from "./Card.vue";
import skills from "./Skills.vue"
import timeLine from "./TimeLine.vue"
import colors from "vuetify/lib/util/colors";

export default {
  components: {
    card,
    skills,
    timeLine
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
