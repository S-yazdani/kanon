<template>
    <v-card style="padding-left: 100px">
        <v-tabs >
            <v-img
                    max-height="62"
                    max-width="110"
                    style="margin-left: -15px"
                    src="../src/assets/pic5.jpg"
            ></v-img>
            <v-tab class="tabstext" >Star</v-tab>
            <v-tab class="tabstext">Wow Stories</v-tab>
            <v-tab class="tabstext">Wowmagazine</v-tab>
            <v-tab class="tabstext">Top User</v-tab>
            <v-tab class="tabstext">About US</v-tab>
            <v-tab class="tabstext">Rules</v-tab>
            <v-tab class="tabstext">Contact US</v-tab>

        </v-tabs>
        <v-card-text style="margin-left: 500px;margin-top: 20px">
            <v-btn
                    width="170px"
                    class="btnCenter"
                    color="#235789"
                    dark
                    @click= "showList1 =!showList1"
            >
                Choose the Level
            </v-btn>
            <div class="shape1"></div>

            <v-card
                    style="position: absolute;z-index: 10"
                    v-if="showList1"
                    class="mx-auto"
                    width="170"
                    tile
            >
                <v-list dense>
                    <v-list-item-group
                            v-model="selectedItem"
                            color="primary"
                    >
                        <v-list-item
                                v-for="(item, i) in items"
                                :key="i"
                        >
                            <v-list-item-content>
                                <v-list-item-title v-text="item.text"></v-list-item-title>
                            </v-list-item-content>
                        </v-list-item>
                    </v-list-item-group>
                </v-list>
            </v-card>
            <v-btn
                    width="170px"
                    color="#0c6ba8"
                    dark
                    class="btnCenter"
                    @click= "showList2 =!showList2"
            >
                Choose the Book
            </v-btn>
            <div class="shape2"></div>
            <v-card
                    style="position: absolute;z-index: 10"
                    v-if="showList2"
                    class="mx-auto"
                    width="170"
                    tile
            >
                <v-list dense>
                    <v-list-item-group
                            v-model="selectedItem"
                            color="primary"
                    >
                        <v-list-item
                                v-for="(item, i) in items"
                                :key="i"
                        >
                            <v-list-item-content>
                                <v-list-item-title v-text="item.text"></v-list-item-title>
                            </v-list-item-content>
                        </v-list-item>
                    </v-list-item-group>
                </v-list>
            </v-card>
            <v-btn
                    width="170px"
                    rounded
                    color="#2d8dab"
                    dark
                    class="btnCenter"
                    @click= "showList3 =!showList3"
            >
                Choose the Lesson
            </v-btn>
            <div class="shape3"></div>
            <v-card
                    style="position: absolute;z-index: 10"
                    v-if="showList3"
                    class="mx-auto"
                    width="170"
                    tile
            >
                <v-list dense>
                    <v-list-item-group
                            v-model="selectedItem"
                            color="primary"
                    >
                        <v-list-item
                                v-for="(item, i) in items"
                                :key="i"
                        >
                            <v-list-item-content>
                                <v-list-item-title v-text="item.text"></v-list-item-title>
                            </v-list-item-content>
                        </v-list-item>
                    </v-list-item-group>
                </v-list>
            </v-card>
            <v-btn
                    width="170px"
                    rounded
                    color="#1c9fc9"
                    dark
                    class="btnCenter"

            >
                Start
            </v-btn>
            <v-img
                    style="margin-right: 10px;margin-top: 70px"
                    max-height="200"
                    max-width="200"
                    src="../src/assets/pic2.jpg"
            ></v-img>
        </v-card-text>
    </v-card>
</template>

<script>
    export default {

        data: () => ({

            showList1:false,
            showList2:false,
            showList3:false,
            items: [
                { text: '1' },
                { text: '2'},
                { text: '3'},
                { text: '4'},
                { text: '5' },
                { text: '6'},
            ],

        }),


        watch: {
            group () {
                this.drawer = false
            },
        },
    }
</script>
<style>
    .tabstext{

        color: #1a237e !important;
        font-family: sans-serif !important;
        font-weight: bolder !important;
        text-transform: capitalize !important;
        font-size: 14px !important;
    }
    .shape1{
        margin-left: 140px;
        width:0;
        height:0;
        border-left: 6px solid transparent;
        border-right: 6px solid transparent;
        border-bottom: 6px solid transparent;
        border-top: 6px solid #235789;
    }
    .shape2{
        margin-left: 22px;
        width:0;
        height:0;
        border-left: 6px solid transparent;
        border-right: 6px solid transparent;
        border-bottom: 6px solid transparent;
        border-top: 6px solid #0c6ba8;
    }
    .shape3{
        margin-left: 135px;
        width:0;
        height:0;
        border-left: 6px solid transparent;
        border-right: 6px solid transparent;
        border-bottom: 6px solid transparent;
        border-top: 6px solid #2d8dab;
    }
    .btnCenter{
        font-size: 13px!important;
        font-family: sans-serif !important;
        text-transform: capitalize !important;
        border-radius: 13px !important;
        margin-top: 10px;
    }
</style>