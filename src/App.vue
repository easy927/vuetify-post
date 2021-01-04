<template>
  <v-app>
    <!--顶部标题栏-->
    <cus_header></cus_header>
    <router-view></router-view>
    <!--页脚-->
    <cus_footer></cus_footer>
  </v-app>
</template>

<script>
    import Home from "./views/home";
    import Cus_header from "./components/cus_header";
    import Cus_footer from "./components/cus_footer";
    export default {
        components: {Cus_footer, Cus_header, Home}
    }
</script>