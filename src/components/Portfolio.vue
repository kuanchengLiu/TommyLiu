<template>
    <v-container>
        <div class="pb-10 pt-5 subTitle">
            PORTFOLIO
        </div>
        <div>
            <v-row>
                <v-card class="mx-auto" max-width="344" v-for="(item, index) in cardItems" :key="index">
                    <v-img :src="item.image" height="200px"></v-img>
                    <v-card-title>
                        {{ item.title }}
                    </v-card-title>
                    <v-card-subtitle>
                        {{ item.subTitle }}
                    </v-card-subtitle>

                    <v-card-actions>
                        <v-btn color="orange lighten-2" text>
                            Explore
                        </v-btn>

                        <v-spacer></v-spacer>

                        <v-btn icon @click="item.show = !item.show">
                            <v-icon>{{ item.show ? 'mdi-chevron-up' : 'mdi-chevron-down' }}</v-icon>
                        </v-btn>
                    </v-card-actions>

                    <v-expand-transition>
                        <div v-show="show">
                            <v-divider></v-divider>

                            <v-card-text>
                                {{ item.details }}
                            </v-card-text>
                        </div>
                    </v-expand-transition>
                </v-card>
            </v-row>

        </div>
    </v-container>
</template>
<script>
export default {
    data: () => {

        return {
            
            cardItems: [
                {
                    image: require("@/assets/SSCP.png"),
                    title: 'SSCP 專業自安人員訓練課程',
                    subTitle: '在上班之餘增進自己的能力....',
                    details: 'test',
                    show: false,
                },
                {
                    image: require("@/assets/webhw.png"),
                    title: '社區管理系統',
                    subTitle: '在上班之餘增進自己的能力....',
                    details: 'test',
                    show: false,
                },
                {
                    image: require("@/assets/SSCP.png"),
                    title: 'SSCP 專業自安人員訓練課程',
                    subTitle: '在上班之餘增進自己的能力....',
                    details: 'test',
                    show: false,
                },
            ],

        };
    },
};
</script>
<style lang="scss" scoped>
@import "../assets/scss/main.scss";
</style>
