<template>
  <div>
    <div class="d-flex align-center px-4 pb-5">
      <div class="text-xxl text-spacing pr-5">My results</div>
      <span class="d-none d-md-block text-gray-2 text-l-2">14 Results</span>
    </div>
    <div class="d-md-none d-flex align-center px-4">
      <button @click="trigerFilter()" class="d-flex align-center">
        <v-icon class="text-blue mr-2">tune</v-icon>
        <div class="text-xl text-bold text-spacing">Filters</div>
      </button>
      <span class="text-gray-2 text-l-2 pl-4">14 Results</span>
    </div>
    <div class="d-flex flex-wrap">
      <v-flex xs12 sm6 lg4 pa-4>
        <div class="item pa-2 pa-md-6">
          <span
            class="item__discount item__discount--green d-flex align-center justify-center text-l"
          >
            99%
          </span>
          <div class="item__size text-l">
            <span class="text-bold text-black">38</span>
            <span class="text-gray-2 pl-1">EU</span>
          </div>
          <img class="item__image" src="../assets/shoes.png" />
          <div class="text-center text-l-2 text-gray">Adidas</div>
          <div class="text-center text-bold text-xl text-black text-spacing">
            Ultraboost
          </div>
        </div>
      </v-flex>
      <v-flex xs12 sm6 lg4 pa-4>
        <div class="item pa-2 pa-md-6">
          <span
            class="item__discount item__discount--yellow d-flex align-center justify-center text-l"
          >
            63%
          </span>
          <div class="item__size text-l">
            <span class="text-bold text-black">38</span>
            <span class="text-gray-2 pl-1">EU</span>
          </div>
          <img class="item__image" src="../assets/shoes.png" />
          <div class="text-center text-l-2 text-gray">Adidas</div>
          <div class="text-center text-bold text-xl text-black text-spacing">
            Ultraboost
          </div>
        </div>
      </v-flex>
      <v-flex xs12 sm6 lg4 pa-4>
        <div class="item pa-6">
          <span
            class="item__discount item__discount--red d-flex align-center justify-center text-l"
          >
            26%
          </span>
          <div class="item__size text-l">
            <span class="text-bold text-black">38</span>
            <span class="text-gray-2 pl-1">EU</span>
          </div>
          <img class="item__image" src="../assets/shoes.png" />
          <div class="text-center text-l-2 text-gray">Adidas</div>
          <div class="text-center text-bold text-xl text-black text-spacing">
            Ultraboost
          </div>
        </div>
      </v-flex>
      <v-flex xs12 sm6 lg4 pa-4>
        <div class="item pa-6">
          <span
            class="item__discount item__discount--green d-flex align-center justify-center text-l"
          >
            99%
          </span>
          <div class="item__size text-l">
            <span class="text-bold text-black">38</span>
            <span class="text-gray-2 pl-1">EU</span>
          </div>
          <img class="item__image" src="../assets/shoes.png" />
          <div class="text-center text-l-2 text-gray">Adidas</div>
          <div class="text-center text-bold text-xl text-black text-spacing">
            Ultraboost
          </div>
        </div>
      </v-flex>
    </div>
  </div>
</template>

<script>
export default {
  name: "CatalogItem",

  methods: {
    trigerFilter() {
      this.$emit("trigerFilter");
    },
  },
};
</script>

<style lang="scss" scoped>
.item {
  position: relative;
  background: $white;
  border-radius: 12px;
  box-shadow: $box-shadow-style;

  &__discount {
    position: absolute;
    top: 8px;
    left: 10px;
    width: 70px;
    height: 70px;
    color: $white;
    border-radius: 100px;

    &--green {
      background-color: $green;
    }

    &--yellow {
      background-color: $yellow;
    }

    &--red {
      background-color: $red;
    }
  }

  &__size {
    position: absolute;
    top: 20px;
    right: 20px;
  }

  &__image {
    display: block;
    margin: 0 auto;
    width: 100%;
    max-width: 250px;
  }

  @media screen and (max-width: ($breakpoint-tablet)) {
    .item {
      &__discount {
        width: 50px;
        height: 50px;
      }
    }
  }

  @media screen and (max-width: ($min-width-mobile)) {
    .item {
      &__discount {
        width: 42px;
        height: 42px;
      }
    }
  }
}
</style>
