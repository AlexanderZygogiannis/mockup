<template>
  <nav class="nav d-flex align-center px-5">
    <div class="d-flex flex-wrap align-center w-100">
      <v-flex xs3>
        <img src="../assets/logo.svg" />
      </v-flex>
      <v-flex xs9>
        <div class="d-flex align-center justify-end">
          <div class="d-none d-sm-flex">
            <Languages />
          </div>
          <div class="d-none d-sm-flex btn-menu btn-menu--white ml-8 mr-4">
            <v-icon class="text-blue text-l-2">contact_support</v-icon>
          </div>
          <div class="btn-menu btn-menu--white mx-sm-4">
            <v-icon class="text-blue text-l-2">shopping_basket</v-icon>
          </div>
          <div
            class="d-none d-sm-flex btn-menu btn-menu--blue mx-4 text-bold text-s text-spacing"
          >
            AM
          </div>
          <div class="d-none d-sm-flex btn-menu btn-menu--white ml-4 mr-8">
            <v-icon class="text-blue text-l-2">pause</v-icon>
          </div>
          <div class="d-flex d-sm-none btn-menu btn-menu--white ml-2">
            <v-icon class="text-blue text-l-2">menu</v-icon>
          </div>
          <div
            class="d-none d-sm-flex text-blue text-xxl text-bold text-spacing"
          >
            End
          </div>
        </div>
      </v-flex>
    </div>
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
  height: 80px;
  margin-bottom: 40px;
  box-shadow: $box-shadow-style;
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

@media screen and (max-width: ($breakpoint-tablet)) {
  .nav {
    height: 65px;
  }
  .btn-menu {
    width: 35px;
    height: 35px;
  }
}
</style>
