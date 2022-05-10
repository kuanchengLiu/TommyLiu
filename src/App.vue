<template>
  <v-app>
    <v-app-bar app color="gray" dark>
      <v-row justify="space-around" class="mr-2">
        <span class="group d-inline-flex pa-2">
          <v-icon>mdi-twitter</v-icon>
          <v-icon>mdi-instagram</v-icon>
          <v-icon>mdi-facebook</v-icon>
          <v-icon>mdi-github-circle</v-icon>
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
      <HelloWorld />
    </v-main>
  </v-app>
</template>

<script>
import HelloWorld from "./components/HelloWorld";

export default {
  name: "App",

  components: {
    HelloWorld,
  },

  data: () => ({
    //s
  }),
};
</script>
