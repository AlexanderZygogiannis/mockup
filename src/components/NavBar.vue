<template>
  <nav class="nav">
    <v-toolbar dense app height="80">
      <div class="d-flex flex-wrap align-center w-100">
        <v-flex sm-3>
          <img src="../assets/logo.svg" />
        </v-flex>
        <v-flex sm-9>
          <div class="d-flex align-center justify-end">
            <Languages />
            <div class="btn-menu btn-menu--white ml-8 mr-4">
              <v-icon class="text-blue text-l-2">contact_support</v-icon>
            </div>
            <div class="btn-menu btn-menu--white mx-4">
              <v-icon class="text-blue text-l-2">shopping_basket</v-icon>
            </div>
            <div
              class="btn-menu btn-menu--blue mx-4 text-bold text-s text-spacing"
            >
              AM
            </div>
            <div class="btn-menu btn-menu--white ml-4 mr-8">
              <v-icon class="text-blue text-l-2">pause</v-icon>
            </div>
            <div class="text-blue text-xxl text-bold text-spacing">End</div>
          </div>
        </v-flex>
      </div>
    </v-toolbar>
  </nav>
</template>

<script>
import Languages from "./Languages.vue";
export default {
  name: "NavBar",
  components: {
    Languages,
  },
};
</script>

<style lang="scss" scoped>
.nav {
  margin-bottom: 40px;
}

.btn-menu {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 50px;
  height: 50px;
  border-radius: 100%;

  &--white {
    background-color: $white;
    box-shadow: $box-shadow-style;

    &:hover {
      cursor: pointer;
      background-color: $blue;
      i {
        color: $white;
      }
    }
  }

  &--blue {
    color: $white;
    background-color: $blue;

    &:hover {
      cursor: pointer;
      color: $blue;
      background-color: $white;
    }
  }
}
</style>
