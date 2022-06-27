<template>
    <v-container>
        <div class="pb-10 pt-5 subTitle">
            SKILLS
        </div>
        <div>
            <v-row class="pl-15 pr-15">
                <v-col>
                    <div class="skill-title"> Front end</div>
                    <div class="text-center">
                        <v-chip class="ma-2" v-for="(item, index) in frontEnd" :key="index" :color="item.color">
                            <v-icon left>
                                {{ item.icon }}
                            </v-icon>
                            {{ item.name }}
                        </v-chip>
                    </div>
                </v-col>
                <v-col>
                    <div class="skill-title"> Back end</div>
                    <div class="text-center">
                        <v-chip class="ma-2" v-for="(item, index) in backEnd" :key="index" :color="item.color">
                            <v-icon left>
                                {{ item.icon }}
                            </v-icon>
                            {{ item.name }}
                        </v-chip>
                    </div>
                </v-col>
                <v-col>
                    <div class="skill-title"> Other </div>
                    <div class="text-center">
                        <v-chip class="ma-2" v-for="(item, index) in other" :key="index" :color="item.color">
                            <v-icon left>
                                {{ item.icon }}
                            </v-icon>
                            {{ item.name }}
                        </v-chip>
                    </div>
                </v-col>
            </v-row>
        </div>
    </v-container>
</template>
<script>
export default {
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
                    icon: "mdi-language-csharp",
                    color: "blue lighten-1"
                }
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
            ]
        };
    },
};
</script>
<style lang="scss" scoped>
@import "../assets/scss/main.scss";
</style>
