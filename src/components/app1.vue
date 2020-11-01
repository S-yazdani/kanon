<template >
    <div class="div">
        <v-container >
            <template >
                <v-card
                        class="mx-auto overflow-hidden"
                        height="660"
                        width="370"

                >
                    <v-app-bar
                            style="background-color: white"
                    >
                        <v-img
                                max-height="62"
                                max-width="110"
                                style="margin-left: -15px"
                                src="../src/assets/pic5.jpg"
                        ></v-img>
                        <v-spacer></v-spacer>
                        <v-img
                                max-height="35"
                                max-width="35"
                                style="margin-left: -10px"
                                src="../src/assets/pic4.jpg"
                        ></v-img>
                        <v-icon style="font-size: 35px;font-weight: bolder;color: #235789;margin-left: 12px" @click.stop="drawer = !drawer">mdi-menu</v-icon>


                    </v-app-bar>

                    <v-navigation-drawer
                            v-model="drawer"
                            absolute
                            right
                            bottom
                            temporary
                            style="background:linear-gradient(-45deg,#003647 90%,#003647 0%);opacity: 90%;width: 200px"
                    >
                        <v-list
                                dense
                        >
                            <v-list-item-group
                                    v-model="group"
                            >
                                <v-list-item>
                                    <v-list-item-title class="fontTextMenuDrawer">Star</v-list-item-title>
                                </v-list-item>

                                <v-list-item>
                                    <v-list-item-title class="fontTextMenuDrawer">Top User</v-list-item-title>
                                </v-list-item>

                                <v-list-item>
                                    <v-list-item-title class="fontTextMenuDrawer">Wow magazine</v-list-item-title>
                                </v-list-item>
                                <v-list-item>
                                    <v-list-item-title class="fontTextMenuDrawer">Wow Stories</v-list-item-title>
                                </v-list-item>
                                <v-list-item>
                                    <v-list-item-title class="fontTextMenuDrawer">About US</v-list-item-title>
                                </v-list-item>
                                <v-list-item>
                                    <v-list-item-title class="fontTextMenuDrawer">Rules</v-list-item-title>
                                </v-list-item>
                                <v-list-item>
                                    <v-list-item-title class="fontTextMenuDrawer">Contact US</v-list-item-title>
                                </v-list-item>
                                <v-list-item>
                                    <v-list-item-title class="fontTextMenuDrawer">Login</v-list-item-title>
                                </v-list-item>
                                <v-list-item>
                                    <v-list-item-title class="fontTextMenuDrawer">Register</v-list-item-title>
                                </v-list-item>
                                <v-list-item>
                                    <v-list-item-title class="fontTextMenuDrawer">Profile</v-list-item-title>
                                </v-list-item>

                            </v-list-item-group>
                        </v-list>

                    </v-navigation-drawer>
                    <v-divider></v-divider>
                    <v-card-text style="margin-left: 80px;margin-top: 20px">
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
                                style="margin-left: -10px;margin-top: 70px"
                                max-height="200"
                                max-width="200"
                                src="../src/assets/pic2.jpg"
                        ></v-img>
                    </v-card-text>
                </v-card>
            </template>

        </v-container>
    </div>

</template>

<script>
    export default {

        data: () => ({
            drawer: false,
            group: null,
            showList1:false,
            showList2:false,
            showList3:false,
            selectedItem: 1,
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
    .div{
        margin-left: 480px;
        overflow-y: hidden;
        overflow-x: hidden;
    }
    .menuDrawer{
        width: 150px;
        height: 580px;
        background: linear-gradient(-45deg,#0D47A1 0%,#0D47A1 0%);
    }
    .fontTextMenuDrawer{
        color: white;
        font-size:20px !important;
        font-family: sans-serif !important
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