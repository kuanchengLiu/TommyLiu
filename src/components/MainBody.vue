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
      <v-timeline>
        <v-timeline-item v-for="(year, i) in years" :key="i" :color="year.color" small>
          <template v-slot:opposite>
            <span :class="`headline font-weight-bold ${year.color}--text`" v-text="year.year"></span>
          </template>
          <div class="py-4">
            <h2 :class="`headline font-weight-light mb-4 ${year.color}--text`">
              {{year.title}}
            </h2>
            <div>
              {{year.detail}}
            </div>
          </div>
        </v-timeline-item>
      </v-timeline>
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
      years: [
        {
          color: 'cyan',
          year: 'now',
          title: '析數智匯股份有限公司 (Advant Analytics Tactics)',
          detail: '去考證照及後端工作內容'
        },
        {
          color: 'green',
          year: '2021-12-01 - 2022-02-18',
          title: 'Military Service',
          detail: '完成兵役'
        },
        {
          color: 'pink',
          year: '2021-06-01 - 2021-11-23',
          title: '析數智匯股份有限公司 (Advant Analytics Tactics)',
          detail: 'APP 工作'
        },
        {
          color: 'amber',
          year: '2018 - 2021',
          title: 'Providence University',
          detail: '專案&實習'
        },
        {
          color: 'orange',
          year: '2016 - 2018',
          title: 'National Keelung Senior High School',
          detail: '社會組轉組'
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/scss/main.scss";
</style>
