<template>
    <v-card class="basil">
        <v-divider></v-divider>
        <centre></centre>
    </v-card>
</template>

<script>
    import Login from "../components/login";
    import Personal from "./personal"
    import Try from "./centre";
    import Editor from "./editor";
    import Centre from "./centre";

    export default {
        components: {Centre, Editor, Try, Login, Personal},
        data() {
            return {
                tab: null,
                transparent: 'rgba(255, 255, 255, 0)'
            }
        },
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
    .v-tabs-bar .v-tab {
         height: 200px !important;
    }
    .v-tab .v-card {
        transition: opacity .4s ease-in-out .2s;
    }

    .v-tab .v-card:not(.on-hover) {
        opacity: 0.2;
    }

    .show-btns {
        color: rgb(255, 255, 255) !important;
    }
</style>
