<template>
  <div>
    <div class="filters">
      <div class="d-flex align-center pb-10">
        <v-icon class="text-blue mr-2">tune</v-icon>
        <div class="text-xl text-bold text-spacing">Filters</div>
      </div>

      <div class="d-flex flex-wrap justify-space-between align-center mb-7">
        <button class="btn btn--blue mt-1">Recommended</button>
        <button class="btn btn--white mt-1">All shoes</button>
      </div>
      <div>
        <v-expansion-panels>
          <v-expansion-panel class="mb-8">
            <v-expansion-panel-header>
              <div class="text-bold text-m text-spacing">Size</div>
            </v-expansion-panel-header>
            <v-expansion-panel-content>
              <v-checkbox v-model="size" label="US" value="us" hide-details />
              <v-checkbox v-model="size" label="EU" value="eu" hide-details />
            </v-expansion-panel-content>
          </v-expansion-panel>
          <v-expansion-panel class="mb-8">
            <v-expansion-panel-header>
              <div class="d-flex align-center justify-space-between">
                <div class="text-bold text-m text-spacing">Brand</div>
                <div class="text-blue text-s">
                  {{ this.brand.length }} Selected
                </div>
              </div>
            </v-expansion-panel-header>
            <v-expansion-panel-content>
              <v-checkbox
                v-model="brand"
                label="New Balance"
                value="New Balance"
                hide-details
              />
              <v-checkbox
                v-model="brand"
                label="Adidas"
                value="Adidas"
                hide-details
              />
              <v-checkbox
                v-model="brand"
                label="Nike Perfomance"
                value="Nike Perfomance"
                hide-details
              />
              <v-checkbox
                v-model="brand"
                label="Reebok"
                value="Reebok"
                hide-details
              />
              <v-checkbox
                v-model="brand"
                label="Asics"
                value="Asics"
                hide-details
              />
              <v-checkbox
                v-model="brand"
                label="Fila"
                value="Fila"
                hide-details
              />
            </v-expansion-panel-content>
          </v-expansion-panel>
        </v-expansion-panels>
        <button @click="clearFilter()" class="text-blue text-l-2 text-spacing">
          Clear all
        </button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "FilterCatalog",
  data() {
    return {
      brand: [],
      size: [],
    };
  },
  methods: {
    clearFilter() {
      this.brand = [];
      this.size = [];
    },
  },
};
</script>

<style lang="scss" scoped>
@import "../scss/buttons";

.filters {
  padding: 45px 55px 42px 41px;
  max-width: 466px;
  box-shadow: $box-shadow-style;

  ::v-deep {
    .v-label {
      font-size: $size-s;
      color: $gray-3;
    }
  }
}

.v-expansion-panel {
  border: 2px solid #585d68;
  border-radius: 12px !important;

  &--active {
    border-radius: 12px !important;
  }
}

@media screen and (max-width: ($max-width-mobile)) {
  .filters {
    box-shadow: unset;
    padding: 20px;
  }
}
</style>
