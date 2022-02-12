<template>
  <header class="p-3 d-flex justify-content-around align-items-center">
    <img
      src="https://www.nicepng.com/png/full/811-8110513_spotify-logo-spotify.png"
    />
    <Search @searchValue="searchValue" />
  </header>
</template>

<script>
import Search from "./Search.vue";
export default {
  name: "Header",

  data() {
    return {
      resultSearch: "",
    };
  },

  methods: {
    searchValue(value) {
      this.$emit("searchValue", value);
      this.resultSearch = value;
    },
  },

  components: {
    Search,
  },
};
</script>

<style scoped>
img {
  width: 75px;
  height: auto;
}
</style>