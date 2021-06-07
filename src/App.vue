<template>
  <v-app>
    <v-app-bar app color="white" dark>
      <div class="d-flex align-center">
        <v-img
          :src="require('./assets/home_logo.jpeg')"
          class="shrink mr-2"
          contain
          transition="scale-transition"
          width="40"
        />
      </div>
      <v-spacer></v-spacer>
    </v-app-bar>

    <v-main>
      <router-view />
    </v-main>
  </v-app>
</template>

<script>
export default {
  name: "App",

  data: () => ({
    //
  }),
};
</script>
<style>
@font-face {
  font-family: "Enjoy";
  src: local("Enjoy"), url("./assets/fonts/Enjoy_Summer.otf");
}
</style>