<template>
  <v-app title="首页">
<!--      <div id="nav">
        <router-link to="/">Home</router-link> |
        <router-link to="/about">About</router-link> |
        <router-link to="/Post">Post</router-link>
      </div>
      <router-view />-->
    <v-main>
      <home/>
    </v-main>

  </v-app>
</template>

<script>
    import Home from "./views/home";
    export default {
        components: {Home}
    }
</script>