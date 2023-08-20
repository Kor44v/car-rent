<template>
  <v-app>
    <v-container>
      <v-row>
        <v-col>
          <NavBar />

          <v-main>
            <router-view />
          </v-main>
        </v-col>
      </v-row>
    </v-container>
  </v-app>
</template>

<script>
import NavBar from "./components/NavBar.vue";

export default {
  name: "App",

  data: () => ({
    //
  }),
  components: {
    NavBar,
  },
};
</script>
<style>
body {
  background-color: #fff;
}
</style>
