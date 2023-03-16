<template>
  <div class="d-flex align-end w-100 mb-10">
    <v-flex sm3>
      <button class="d-flex align-center justify-end text-blue text-m w-100">
        <v-icon class="text-m text-blue">arrow_back_ios</v-icon>
        <span>BACK TO MY SCAN</span>
      </button>
    </v-flex>
    <v-flex sm9>
      <div class="wrapper px-4">
        <div
          class="search-bar d-flex align-center text-l-2 text-gray text-spacing"
        >
          <v-icon class="text-xxl">search</v-icon>
          <input class="w-100" type="text" placeholder="Search shoes" />
        </div>
      </div>
    </v-flex>
  </div>
</template>

<script>
export default {
  name: "SearchBar",
};
</script>

<style lang="scss" scoped>
.search-bar {
  padding: 10px 15px;
  border-radius: 5px;
  box-shadow: $box-shadow-style;
}
</style>
