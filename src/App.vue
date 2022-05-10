<template>
  <v-app>
    <v-app-bar app color="gray" dark>
      <v-row justify="space-around" class="mr-2">
        <span class="group d-inline-flex pa-2">
          <v-icon class="pa-2">mdi-twitter</v-icon>
          <v-icon class="pa-2">mdi-instagram</v-icon>
          <v-icon class="pa-2">mdi-facebook</v-icon>
          <v-icon class="pa-2">mdi-github</v-icon>
        </span>
      </v-row>
      <v-item> </v-item>
      <v-spacer></v-spacer>

      <v-btn
        href="https://github.com/vuetifyjs/vuetify/releases/latest"
        target="_blank"
        text
      >
        <span class="mr-2">Latest Release</span>
        <v-icon>mdi-open-in-new</v-icon>
      </v-btn>
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
    MainBody
  },

  data: () => ({
    //s
  }),
};
</script>
