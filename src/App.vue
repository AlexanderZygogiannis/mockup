<template>
  <v-app>
    <NavBar />
    <v-content>
      <v-layout>
        <v-flex sm4> Filter </v-flex>
        <v-flex sm8> List </v-flex>
      </v-layout>
    </v-content>
  </v-app>
</template>

<script>
import NavBar from "./components/NavBar.vue";

export default {
  name: "App",
  components: {
    NavBar,
  },

  data: () => ({
    //
  }),
};
</script>
