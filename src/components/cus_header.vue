<template>
    <v-card class="basil">
        <v-card-title class="text-center justify-center py-2" :aria-level="0">
            <v-spacer></v-spacer>
            <router-link to="/">
                <v-avatar style="height:50px;width: 75px">
                    <img src="../static/pics/logo-min.png"
                         alt="jinshu"
                    ></v-avatar>
            </router-link>

            <v-spacer></v-spacer>
            <v-text-field
                    v-model="search"
                    append-icon="mdi-magnify"
                    label="搜索"
                    single-line
                    hide-details
            ></v-text-field>
            <v-spacer></v-spacer>

            <!--<router-link to="/personal">
            </router-link>-->
            <v-avatar @click="doLogin">
                <img src="https://cdn.vuetifyjs.com/images/john.jpg"
                     alt="John"
                ></v-avatar>
            <login v-if="hasLogin"></login>
            <router-link v-if="hasPerson" to="/personal">
            </router-link>
            <v-spacer></v-spacer>
        </v-card-title>
    </v-card>
</template>

<script>
    import Login from "./login";

    export default {
        name: 'cus_header',
        components: {Login},
        data() {
            return {
                search: '',
                hasLogin:false,
                hasPerson:false
            }
        },
        methods: {

            doLogin() {
                console.log('doLogin:'+this.hasLogin),
                this.hasLogin = true
            }
        }
    }
</script>

<style>
    /* Helper classes */
    .basil {
        background-color: #FFFBE6 !important;
    }

    .basil--text {
        color: #356859 !important;
    }

    a {
        text-decoration: none;
    }

    .router-link-active {
        text-decoration: none;
    }

</style>
