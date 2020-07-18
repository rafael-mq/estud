<template>
  <v-app>
    <!-- <v-app-bar app color="primary" dark></v-app-bar> -->
    <Navigation />
    <v-main transition="slide-x-transition">
      <router-view></router-view>
    </v-main>
  </v-app>
</template>

<script>
import Navigation from "./components/Navigation";

export default {
  name: "App",

  components: {
    Navigation
  },

  data: () => ({
    //
  })
};
</script>
