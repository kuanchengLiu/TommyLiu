<template>
    <v-container>
        <div class="pb-10 pt-5 subTitle">
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
                            I'm a thing. But, like most politicians, he promised more than he could deliver. You won't
                            have time for
                            sleeping, soldier, not with all the bed making you'll be doing. Then we'll go with that data
                            file! Hey,
                            you add a one and two zeros to that or we walk! You're going to do his laundry? I've got to
                            find a way to
                            escape.
                        </v-card-text>
                    </div>
                </v-expand-transition>
            </v-card>
        </div>
    </v-container>
</template>
<script>
import xd from "@/assets/xd.png"
export default {

    icons: {
        xd: {
            component: xd,
            props: {
                name: "xd"
            }
        },
    },
    data: () => {

        return {
            frontEnd: [
                {
                    name: "Vue js",
                    icon: "mdi-vuejs",
                    color: "green darken-1"
                },
                {
                    name: "Vuetify",
                    icon: "mdi-vuetify",
                    color: "primary"
                },
                {
                    name: "Angular",
                    icon: "mdi-angular",
                    color: "red"
                },
                {
                    name: "Sass",
                    icon: "mdi-sass",
                    color: "#bf4080"
                },
                {
                    name: "Javascript",
                    icon: "mdi-language-javascript",
                    color: "yellow"
                },
            ],
            backEnd: [
                {
                    name: "ASP.NET",
                    icon: "mdi-dot-net",
                    color: "blue lighten-1"
                },
                {
                    name: "Docker",
                    icon: "mdi-docker",
                    color: "primary"
                },
                {
                    name: "Linux",
                    icon: "mdi-linux",
                    color: "primary"
                },
                {
                    name: "RabbitMQ",
                    icon: xd,
                    color: "orange",
                    ispng: true
                },
            ],
            other: [
                {
                    name: "Android",
                    icon: "mdi-android",
                    color: "green"
                },
                {
                    name: "Git",
                    icon: "mdi-git",
                    color: "orange"
                },
                {
                    name: "Java",
                    icon: "mdi-language-java",
                    color: "gray"
                },
                {
                    name: "Azure DevOps",
                    icon: "mdi-microsoft-azure-devops",
                    color: "primary"
                },
            ]
        };
    },
};
</script>
<style lang="scss" scoped>
@import "../assets/scss/main.scss";
</style>
