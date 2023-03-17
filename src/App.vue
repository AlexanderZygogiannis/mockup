<template>
  <v-app>
    <NavBar />
    <SearchBar />
    <v-main>
      <div class="wrapper px-5">
        <v-navigation-drawer
          v-model="drawer"
          absolute
          left
          temporary
          width="90%"
        >
          <Filters />
        </v-navigation-drawer>
      </div>
      <div class="d-flex px-3">
        <v-flex d-none d-md-block md4 lg3>
          <Filters />
        </v-flex>
        <v-flex md8 lg9>
          <div class="wrapper">
            <Catalog @trigerFilter="togleFilter" />
          </div>
        </v-flex>
      </div>
    </v-main>
  </v-app>
</template>

<script>
import NavBar from "./components/NavBar.vue";
import Catalog from "./components/Catalog.vue";
import Filters from "./components/Filters.vue";
import SearchBar from "./components/SearchBar.vue";

export default {
  name: "App",
  components: {
    NavBar,
    Filters,
    Catalog,
    SearchBar,
  },

  data: () => ({
    drawer: false,
  }),

  methods: {
    togleFilter() {
      this.drawer = !this.drawer;
    },
  },
};
</script>

<style lang="scss">
@import url("https://fonts.googleapis.com/css2?family=Heebo:wght@400;500&display=swap");

html,
body {
  font-family: "Heebo", sans-serif;
  font-weight: 400;
  color: $black;
}

#app {
  font-family: "Heebo", sans-serif;
  font-weight: 400;
}
</style>
