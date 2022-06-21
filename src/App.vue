<template>
  <v-app>
    <v-app-bar app color="grey lighten-4" dark>
      <div class="fill-width" align="center">
        <p class="blog-name">Tommy Liu</p>
      </div>
      <v-row justify="space-around" class="mr-2">
        <span class="group d-inline-flex pa-2">
          <v-btn icon href="https://twitter.com/liutommy880108">
            <v-icon color="grey darken-1" class="pa-2">mdi-twitter</v-icon>
          </v-btn>
          <v-btn icon href="https://www.instagram.com/tom__liu/">
            <v-icon color="grey darken-1" class="pa-2">mdi-instagram</v-icon>
          </v-btn>
          <v-btn icon href="https://www.facebook.com/tommy.liu.3192">
            <v-icon color="grey darken-1" class="pa-2">mdi-facebook</v-icon>
          </v-btn>
          <v-btn icon href="https://github.com/kuanchengLiu">
            <v-icon color="grey darken-1" class="pa-2">mdi-github</v-icon>
          </v-btn>
        </span>
      </v-row>
      <v-row justify="space-around" class="mr-2">
        <span class="group d-inline-flex pa-2">
          <v-btn icon>
            <p class="blog-appbar-col pa-2">home</p>
          </v-btn>
          <v-btn icon>
            <p class="blog-name pa-2">about</p>
          </v-btn>
          <v-btn icon>
            <p class="blog-name pa-2">tec</p>
          </v-btn>
          <v-btn icon>
            <p class="blog-name pa-2">travel</p>
          </v-btn>
        </span>
      </v-row>
    </v-app-bar>
    <div>
      <v-main>
        <MainBody />
      </v-main>
    </div>

    <div class="pt-1">
      <v-footer dark padless>
        <v-card flat tile class="blue-grey lighten-1 white--text text-center">
          <v-card-text>
            <v-btn
              v-for="icon in icons"
              :key="icon"
              class="mx-4 white--text"
              icon
            >
              <v-icon size="24px">
                {{ icon }}
              </v-icon>
            </v-btn>
          </v-card-text>

          <v-card-text class="white--text pt-0">
            Phasellus feugiat arcu sapien, et iaculis ipsum elementum sit amet.
            Mauris cursus commodo interdum. Praesent ut risus eget metus luctus
            accumsan id ultrices nunc. Sed at orci sed massa consectetur
            dignissim a sit amet dui. Duis commodo vitae velit et faucibus.
            Morbi vehicula lacinia malesuada. Nulla placerat augue vel ipsum
            ultrices, cursus iaculis dui sollicitudin. Vestibulum eu ipsum vel
            diam elementum tempor vel ut orci. Orci varius natoque penatibus et
            magnis dis parturient montes, nascetur ridiculus mus.
          </v-card-text>

          <v-divider></v-divider>

          <v-card-text class="white--text">
            {{ new Date().getFullYear() }} — <strong>Vuetify</strong>
          </v-card-text>
        </v-card>
      </v-footer>
    </div>
  </v-app>
</template>

<script>
import MainBody from "./components/MainBody.vue";

export default {
  name: "App",

  components: {
    MainBody,
  },

  data: () => ({
    icons: ["mdi-facebook", "mdi-twitter", "mdi-linkedin", "mdi-instagram"],
  }),
};
</script>

<style lang="scss" scoped>
@import "./assets/scss/color.scss";
@import "./assets/scss/main.scss";
</style>
