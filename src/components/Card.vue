<template>
    <v-card class="mx-auto" max-width="50%" outlined elevation="24" color="grey lighten-3">
        <v-list-item two-line>
            <v-list-item-content>
                <v-list-item-title class="text-h5 mb-1"> 劉冠呈 Tommy</v-list-item-title>
                <v-list-item-subtitle>Back end Developer/Android Developer</v-list-item-subtitle>
                <div class="pt-5">
                    <v-row>
                        <v-col class="fill-width" justify="space-around">
                            <div class="introduction-title">Phone</div>
                            <div class="body-1">0975738390</div>
                        </v-col>
                        <v-col class="fill-width" justify="space-around">
                            <div class="introduction-title">Email</div>
                            <div class="body-1">tommyliu0108@gmailcom</div>
                        </v-col>
                    </v-row>
                </div>
                <div class="pt-5">
                    <v-row>
                        <v-col class="fill-width" justify="space-around">
                            <div class="introduction-title">Address</div>
                            <div class="body-1">Taiwan Taipei City</div>
                        </v-col>
                        <v-col class="fill-width" justify="space-around">
                            <div class="introduction-title">Birth</div>
                            <div class="body-1">January 8th, 1999</div>
                        </v-col>
                    </v-row>
                </div>
                <div class="pt-5">
                    <v-row>
                        <v-col class="fill-width" justify="space-around">
                            <div class="introduction-title">Hobby</div>
                            <div class="body-1">Travel(specially Japan), reading light novels and watch NBA games</div>
                        </v-col>
                    </v-row>
                </div>
            </v-list-item-content>

            <v-list-item-avatar tile size="50%" max-height="300px">
                <v-img :src="slideImage[0]"></v-img>
            </v-list-item-avatar>
        </v-list-item>

        <!-- <v-card-actions>
            <v-btn outlined rounded text> Button </v-btn>
        </v-card-actions> -->
    </v-card>
</template>
<script>
export default {
  data: () => {
    return {
      slideImage: [require("@/assets/me.jpg")],
    };
  },
};
</script>
<style lang="scss" scoped>


@import "../assets/scss/main.scss";
</style>
