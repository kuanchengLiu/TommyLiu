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
                            <ol>
                                <li v-for="(item) in year.detail" :key="item">
                                    <p class="experence-main">{{ item.main }}</p>
                                    <ul>
                                        <li class="experence-sub" v-for="(index) in item.sub" :key="index">
                                            {{ index }}
                                        </li>
                                    </ul>
                                </li>
                            </ol>
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
                                main: "SSCP 資安專業人員認證課程",
                                sub: [
                                    "實作"
                                ]
                            },
                            {
                                main: "某國際零售廠電商串流平台 Web 設計",
                                sub: [
                                    "工作內容: 70% web 後端服務開發 20% web UI設計 10% 使用者操作說明",
                                    "蝦皮、momo、yahoo等電商平台API串接",
                                    "以RabbitMQ Message Queue 解決多平台資料非同步串流處理",
                                    "平台 UI 設計"
                                ]
                            },
                        ]

                },
                {
                    color: 'green',
                    year: '2021.12 - 2022.02',
                    title: '陸軍',
                    workFor: "軍隊",
                    detail:
                        [
                            {
                                main: "義務役",
                                sub: [
                                    "第一階段於斗煥坪服役",
                                    "第二階段則在成功嶺服役"
                                ],
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
                                main: "某光學工廠 MES 系統後台(Windows Form)",
                                sub: [
                                    "工作內容: 80% windows後台開發 20%現場人員訪談及使用教學",
                                    "IIS windows service架設",
                                    "windows form 後台畫面及功能開發",
                                ]
                            },
                            {
                                main: "MES 即時生產狀態網頁開發",
                                sub: [
                                    "工作內容: 50% web 網頁前端設計 50% stored procedure撰寫",
                                    "現場工單進行狀況的視覺化設計",
                                    "介接 Oracle ERP 資料庫",
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
                                main: "某光學工廠 MES APP 線上開報工專案(Android App)",
                                sub: [
                                    "工作內容: 70% APP 程式開發 30%現場人員訪談、使用環境測試及使用教學",
                                    "MES 報工 APP 設計及開發",
                                    "取代繁複的紙本作業內容",
                                ]
                            },
                        ]
                },
                {
                    color: 'orange',
                    year: '2018.07 - 2021.06',
                    title: '靜宜大學 資訊工程學系',
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
