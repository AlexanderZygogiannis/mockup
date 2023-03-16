<template>
  <v-app>
    <NavBar />
    <SearchBar />
    <v-content>
      <div class="d-flex px-3">
        <v-flex sm3>
          <Filters />
        </v-flex>
        <v-flex sm9>
          <div class="wrapper">
            <Catalog />
          </div>
        </v-flex>
      </div>
    </v-content>
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
    //
  }),
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
