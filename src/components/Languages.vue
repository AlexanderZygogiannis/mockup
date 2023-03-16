<template>
  <v-menu offset-y max-width="230" nudge-left="50%" open-on-hover>
    <template v-slot:activator="{ on, attrs }">
      <v-btn v-bind="attrs" v-on="on" height="40" width="40" depressed plain>
        <img class="images" :src="flag" :alt="items[selectedCountry].title" />
      </v-btn>
    </template>
    <v-list>
      <v-list-item-group v-model="selectedCountry">
        <v-list-item v-for="(item, index) in items" :key="index">
          <v-list-item-title>{{ item.title }}</v-list-item-title>
        </v-list-item>
      </v-list-item-group>
    </v-list>
  </v-menu>
</template>

<script>
export default {
  name: "LanguagesMenu",
  data: () => ({
    selectedCountry: 0,
    items: [
      { title: "Dutch", flag: "nl.png" },
      { title: "Chinice", flag: "cn.png" },
      { title: "Russian", flag: "ru.png" },
      { title: "Greek", flag: "gr.png" },
    ],
  }),
  computed: {
    flag() {
      const imgSrc = require(`@/assets/flags/${
        this.items[this.selectedCountry].flag
      }`);

      return imgSrc;
    },
  },
};
</script>

<style lang="scss" scoped>
.images {
  width: 40px;
  height: 40px;
}

.v-menu {
  &__content {
    width: 229px;
    border-radius: 12px;
    box-shadow: $box-shadow-style;
  }
}

.v-list {
  padding: 26px;
}
.v-list-item {
  line-height: 32px;
  min-height: unset;
  padding: 15px 0;

  &--active,
  &:hover {
    color: $blue;

    &::before {
      content: none;
    }
  }

  &:first-child {
    padding-top: 0;
  }

  &:last-child {
    padding-bottom: 0;
  }

  &__title {
    letter-spacing: $letter-spacing;
    font-size: $size-l-2;
  }
}
</style>
