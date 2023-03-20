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
              <v-checkbox
                v-for="size in sizes"
                :key="size.id"
                v-model="selectedsize"
                :label="size.name"
                :value="size.value"
                on-icon="mdi-checkbox-marked-circle"
                off-icon="mdi-checkbox-blank-circle-outline"
                hide-details
              />
            </v-expansion-panel-content>
          </v-expansion-panel>
          <v-expansion-panel class="mb-8">
            <v-expansion-panel-header>
              <div class="d-flex align-center justify-space-between">
                <div class="text-bold text-m text-spacing">Brand</div>
                <div class="text-blue text-s">
                  {{ this.selectedBrand.length }} Selected
                </div>
              </div>
            </v-expansion-panel-header>
            <v-expansion-panel-content>
              <v-checkbox
                v-for="brand in brands"
                :key="brand.id"
                v-model="selectedBrand"
                :label="brand.value"
                :value="brand.value"
                on-icon="mdi-checkbox-marked-circle"
                off-icon="mdi-checkbox-blank-circle-outline"
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
      selectedBrand: [],
      selectedsize: [],
      sizes: [
        { id: 1, value: "eu", name: "EU" },
        { id: 2, value: "us", name: "US" },
      ],
      brands: [
        { id: 1, value: "Adidas" },
        { id: 2, value: "New Balance" },
        { id: 3, value: "Nike Perfomance" },
        { id: 4, value: "Reebok" },
        { id: 5, value: "Asics" },
        { id: 6, value: "Fila" },
        { id: 7, value: "Jordan" },
        { id: 8, value: "Testoni" },
        { id: 9, value: "Converse" },
        { id: 10, value: "Berluti" },
        { id: 11, value: "Johnson and Murphy" },
        { id: 12, value: "Timberland" },
        { id: 13, value: "Clarks" },
        { id: 14, value: "VANS" },
        { id: 15, value: "Puma" },
        { id: 16, value: "Crocs" },
        { id: 17, value: "Calvin Klein" },
        { id: 19, value: "Lacoste" },
        { id: 20, value: "By Hudson" },
        { id: 21, value: "Columbia" },
        { id: 22, value: "New Balance" },
        { id: 23, value: "Under Armour" },
        { id: 24, value: "Bogs" },
      ],
    };
  },
  methods: {
    clearFilter() {
      this.selectedBrand = [];
      this.selectedsize = [];
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

    .v-expansion-panel-content {
      padding-bottom: 10px;

      &__wrap {
        max-height: 250px;
        overflow-y: auto;
      }
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

    ::v-deep {
      .v-label {
        font-size: 12px;
      }

      .v-input {
        &--selection-controls {
          margin-top: 10px;
        }
      }
    }
  }
}
</style>
