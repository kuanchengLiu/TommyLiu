<template>
    <v-card class="mx-auto" max-width="50%" outlined elevation="24" color="grey lighten-3">
        <div v-if="windowWidth < 850">
            <v-img class="white--text align-end" height="200px" :src="slideImage[0]">
                <v-card-title>劉冠呈 Tommy</v-card-title>
            </v-img>
            <div class="pa-1">

                <div class="pt-4">
                    <v-row>
                        <v-col class="fill-width" justify="space-around">
                            <div class="introduction-title">Phone</div>
                            <div class="body-1">0975738390</div>
                        </v-col>
                        <v-col class="fill-width" justify="space-around">
                            <div class="introduction-title">Email</div>
                            <div class="body-1">tommyliu0108@gmail.com</div>
                        </v-col>
                    </v-row>
                </div>
                <div class="pt-5">
                    <v-row>
                        <v-col class="fill-width" justify="space-around">
                            <div class="introduction-title">Address</div>
                            <div class="body-1">Taiwan, Taipei City</div>
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
            </div>

        </div>
        <v-list-item two-line v-else>
            <v-list-item-content>
                <v-list-item-title class="text-h5 mb-1"> 劉冠呈 Tommy </v-list-item-title>
                <v-list-item-subtitle>Back end Developer | Android Developer | Program Designer</v-list-item-subtitle>
                <div class="pt-5">
                    <v-row>
                        <v-col class="fill-width" justify="space-around">
                            <div class="introduction-title">Phone</div>
                            <div class="body-1">0975738390</div>
                        </v-col>
                        <v-col class="fill-width" justify="space-around">
                            <div class="introduction-title">Email</div>
                            <div class="body-1">tommyliu0108@gmail.com</div>
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



    </v-card>
</template>
<script>
export default {
    data: () => {
        return {
            slideImage: [require("@/assets/me.jpg")],
            windowWidth: window.innerWidth,
        };
    },
    watch: {
        windowHeight(newHeight, oldHeight) {
            this.windowWidth = `it changed to ${newHeight} from ${oldHeight}`;
        }
    },

    mounted() {
        this.$nextTick(() => {
            window.addEventListener('resize', this.onResize);
        })
    },

    beforeDestroy() {
        window.removeEventListener('resize', this.onResize);
    },

    methods: {
        onResize() {
            this.windowWidth = window.innerWidth
        }
    }
};
</script>
<style lang="scss" scoped>
@import "../assets/scss/main.scss";
</style>
