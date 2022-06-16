<template>
  <v-main>
    <v-container fluid>
      <div>
        <v-carousel>
          <v-carousel-item
            v-for="n in image"
            :key="n"
            :src="n"
            reverse-transition="fade-transition"
            transition="fade-transition"
          >
            <v-row class="fill-height" align="center" justify="center">
              <v-col class="fill-width" align="center" justify="center">
                <div class="text title">Tommy's bolg</div>
                <div class="h5 title">
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
    </v-container>
  </v-main>
</template>

<script>
import colors from "vuetify/lib/util/colors";

export default {
  data() {
    return {
      image: [require("@/assets/736461.png")],
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
