<template>
    <v-card flex
            class="mx-auto"
            max-width="1200"
            min-height="900"
    >
        <v-spacer></v-spacer>
        <v-container fluid>
            <v-row dense>
                <v-col :cols="11">
                    <v-row>
                        <v-col
                                v-for="card in AboveCards"
                                :key="card.title"
                                :cols="card.flex"
                        >
                            <v-card>
                                <router-link to="/post/id">
                                    <v-img
                                            :src="card.src"
                                            class="white--text align-end"
                                            gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
                                            height="100px"

                                    >
                                        <v-card-title v-text="card.title"></v-card-title>
                                    </v-img>

                                </router-link>

                                <v-card-actions>
                                    <span>2020年12月23日 8:59:32</span>
                                    <v-spacer></v-spacer>
                                    <span>阅读量：231</span>
                                    <!--<v-btn icon>
                                        <v-icon color="red">mdi-heart</v-icon>
                                    </v-btn>

                                    <v-btn icon>
                                        <v-icon color="yellow">mdi-bookmark</v-icon>
                                    </v-btn>

                                    <v-btn icon>
                                        <v-icon color="blue">mdi-share-variant</v-icon>
                                    </v-btn>-->
                                </v-card-actions>
                            </v-card>
                        </v-col>
                        <v-col
                                v-for="card in DownCards"
                                :key="card.title"
                                :cols="card.flex"
                        >
                            <v-card>
                                <router-link to="/post/+card.id">
                                    <v-card-actions>
                                        <span class="title">{{card.title}}</span>
                                        <v-spacer></v-spacer>

                                        <span>2020年12月23日 8:59:32</span>
                                    </v-card-actions>

                                </router-link>


                            </v-card>
                        </v-col>
                    </v-row>
                </v-col>
                <v-col :cols="1">
                    <v-row>
                        <v-speed-dial
                                v-model="fab"
                                direction="right"
                                :open-on-hover="hover"
                                :transition="transition"
                        >
                            <template v-slot:activator>
                                <v-btn
                                        v-model="fab"
                                        color="blue darken-2"
                                        dark
                                        fab
                                >
                                    <v-icon v-if="fab">mdi-close</v-icon>
                                    <v-icon v-else>mdi-filter</v-icon>
                                </v-btn>
                            </template>
                            <v-btn
                                    fab
                                    dark
                                    small
                                    color="green"
                            >
                                <v-icon>mdi-calendar</v-icon>
                            </v-btn>
                            <v-btn
                                    fab
                                    dark
                                    small
                                    color="indigo"
                            >
                                <v-icon color="red">mdi-heart</v-icon>
                            </v-btn>
                            <v-btn
                                    fab
                                    dark
                                    small
                                    color="red"
                            >
                                <v-icon>mdi-read</v-icon>
                            </v-btn>
                        </v-speed-dial>
                    </v-row>
                    <router-link to="/editor">
                        <v-row class="pencil">
                            <v-tooltip bottom>
                                <template v-slot:activator="{ on, attrs }">
                                    <v-btn
                                            fab
                                            dark
                                            color="green"
                                            v-bind="attrs"
                                            v-on="on"
                                    >
                                        <v-icon>mdi-pencil</v-icon>
                                    </v-btn>
                                </template>
                                <span>开始写信吧！</span>
                            </v-tooltip>
                        </v-row>
                    </router-link>
                </v-col>

            </v-row>

            <v-spacer></v-spacer>
            <div class="text-center">
                <v-pagination
                        v-model="page"
                        :length="pages"
                        :total-visible="7"
                        circle
                ></v-pagination>
            </div>

        </v-container>
    </v-card>
</template>

<script>
    export default {
        name:'centre',
        data: () => ({
            AboveCards: [
                {title: '你好啊，王小波', src: 'https://cdn.vuetifyjs.com/images/cards/house.jpg', flex: 12},
                {title: '祭十二郎文', src: require("../static/pics/snow.jpg"), flex: 6},
                {title: '最后一课', src: 'https://cdn.vuetifyjs.com/images/cards/plane.jpg', flex: 6},
            ],
            DownCards: [
                {title: '放走的俘虏光着膀子跑回来了', src: 'https://cdn.vuetifyjs.com/images/cards/plane.jpg', flex: 12},
                {title: '在尸首遍陈的战场，我会梦见您的倩影', src: 'https://cdn.vuetifyjs.com/images/cards/plane.jpg', flex: 12},
                {title: '我要往前走', src: 'https://cdn.vuetifyjs.com/images/cards/plane.jpg', flex: 12},
                {title: '我有时真想拉你一同死去', src: 'https://cdn.vuetifyjs.com/images/cards/plane.jpg', flex: 12},
                {title: '好像我成为了中国最佳的工程师', src: 'https://cdn.vuetifyjs.com/images/cards/plane.jpg', flex: 12},
                {title: '李白写给韩荆州', src: 'https://cdn.vuetifyjs.com/images/cards/plane.jpg', flex: 12},
                {title: '好像我成为了最佳的工程师', src: 'https://cdn.vuetifyjs.com/images/cards/plane.jpg', flex: 12},
            ],
            page:1,
            pages:16,
            fab: false,
            fling: false,
            hover: false,
            tabs: null,
            transition: 'slide-y-reverse-transition',
        }),
        computed: {
            activeFab () {
                switch (this.tabs) {
                    case 'one': return { class: 'purple', icon: 'account_circle' }
                    case 'two': return { class: 'red', icon: 'edit' }
                    case 'three': return { class: 'green', icon: 'keyboard_arrow_up' }
                    default: return {}
                }
            },
        },
    }
</script>
<style>
    .theme--light .v-card{
        background-color: #FFFBE6;
        color: #2196f3;
    }
    .row--dense > .col, .row--dense > [class*=col-11] {
        padding: 8px;
    }
    .row--dense > .col, .row--dense > [class*=col-1] {
        padding: 0px 0px 0px 20px;
    }

    .v-sheet.v-card:not(.v-sheet--outlined) {
        box-shadow: 1px 1px 1px -2px rgba(0, 0, 0, 0.2), 1px 1px 2px 0px rgba(0, 0, 0, 0.0), 0px 1px 1px 0px rgba(0, 0, 0, 0.12);
    }

    .v-speed-dial {
        padding: 12px 0px 0px 12px;
    }
    .pencil {
        padding: 34px 0px 0px 12px;
    }
</style>