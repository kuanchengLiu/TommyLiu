<template>
  <v-app>
    <v-app-bar app color="grey lighten-4" dark>
      <div class="fill-width" align="center">
        <p class="blog-name">Tommy's Blog</p>
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
      <v-row justify="space-around"> </v-row>
      <v-item> </v-item>
      <v-spacer></v-spacer>
    </v-app-bar>

    <v-main>
      <MainBody />
    </v-main>
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
    //s
  }),
};
</script>

<style lang="scss" scoped>
@import "./assets/scss/color.scss";
@import "./assets/scss/main.scss";
</style>
