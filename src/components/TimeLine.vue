<template>
    <v-container>
        <div class="pb-10 pt-10 subTitle">
            EXPERIENCE & EDUCATION
        </div>
        <div class="px-15">
            <v-timeline>
                <v-timeline-item v-for="(year, i) in years" :key="i" :color="year.color" small>
                    <template v-slot:opposite>
                        <span :class="`headline font-weight-bold ${year.color}--text`" v-text="year.year"></span>
                    </template>
                    <v-card class="elevation-2">
                        <v-card-title :class="`headline font-weight-light mb-4 ${year.color}--text`">
                            {{ year.title }}
                        </v-card-title>
                        <v-card-subtitle :class="`headline font-weight-light mb-4 ${year.color}--text`">
                            {{ year.workFor }}
                        </v-card-subtitle>
                        <v-card-text class="text-h6">
                            {{ year.detail }}
                        </v-card-text>
                    </v-card>
                </v-timeline-item>
            </v-timeline>
        </div>
    </v-container>
</template>
<script>
export default {
    data: () => {
        return {
            show: false,
            years: [
                {
                    color: 'cyan',
                    year: '2022.02 - Present',
                    title: '程式設計師',
                    workFor: "析數智匯股份有限公司 (Advant Analytics Tactics)",
                    detail:
                        [
                            {
                                main: "證照及後端",
                                sub: [
                                    "減少40%的人工資料處理作業",
                                    "MES 報工 APP 設計及開發",
                                    "取代繁複的紙本作業內容",
                                    "直接產生工具使用歷程報表",
                                    "ORACLE ERP及生管資料對接"
                                ]
                            },
                        ],
                },
                {
                    color: 'green',
                    year: '2021.12 - 2022.02',
                    title: 'Military Service',
                    workFor: "Army",
                    detail:
                        [
                            {
                                main: "兵役",
                                sub: [
                                    "減少40%的人工資料處理作業",
                                    "MES 報工 APP 設計及開發",
                                    "取代繁複的紙本作業內容",
                                    "直接產生工具使用歷程報表",
                                    "ORACLE ERP及生管資料對接"
                                ]
                            },
                        ]
                },
                {
                    color: 'pink',
                    year: '2021.06 - 2021.12',
                    title: 'APP 工程師',
                    workFor: "析數智匯股份有限公司 (Advant Analytics Tactics)",
                    detail:
                        [
                            {
                                main: "協助某光學工廠導入 MES 系統(Windows Form)",
                                sub: [
                                    "減少40%的人工資料處理作業",
                                    "MES 報工 APP 設計及開發",
                                    "取代繁複的紙本作業內容",
                                    "直接產生工具使用歷程報表",
                                    "ORACLE ERP及生管資料對接"
                                ]
                            },
                            {
                                main: "即時生產報工網頁開發",
                                sub: [
                                    "減少40%的人工資料處理作業",
                                    "MES 報工 APP 設計及開發",
                                    "取代繁複的紙本作業內容",
                                    "直接產生工具使用歷程報表",
                                    "ORACLE ERP及生管資料對接"
                                ]
                            }
                        ]
                },
                {
                    color: 'amber',
                    year: '2021.02 - 2021.06',
                    title: '實習生',
                    workFor: "析數智匯股份有限公司 (Advant Analytics Tactics)",
                    detail:
                        [
                            {
                                main: "協助某光學工廠導入 MES 系統(Android App)",
                                sub: [
                                    "減少40%的人工資料處理作業",
                                    "MES 報工 APP 設計及開發",
                                    "取代繁複的紙本作業內容",
                                    "直接產生工具使用歷程報表",
                                    "ORACLE ERP及生管資料對接"
                                ]
                            },
                        ]
                },
                {
                    color: 'orange',
                    year: '2018.07 - 2021.06',
                    title: '靜宜大學',
                    detail:
                        [
                            {
                                main: "專案及社團",
                                sub: [
                                    "減少40%的人工資料處理作業",
                                    "MES 報工 APP 設計及開發",
                                    "取代繁複的紙本作業內容",
                                    "直接產生工具使用歷程報表",
                                    "ORACLE ERP及生管資料對接"
                                ]
                            },
                        ]
                },
            ],
        };
    },
};
</script>
<style lang="scss" scoped>
@import "../assets/scss/main.scss";
</style>
