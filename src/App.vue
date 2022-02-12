<template>
  <div class="container-fluid">
    <Header class="background-header" @searchValue="searchValue" />
    <Main />
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Main from "./components/Main.vue";
export default {
  name: "App",

  data() {
    return {
      resultSearch: "All",
    };
  },

  methods: {
    searchValue(value) {
      this.resultSearch = value;
    },
  },
  components: {
    Header,
    Main,
  },
};
</script>

<style lang="scss">
.background-header {
  background-color: rgb(46, 58, 70);
}
@import "./assets/sass/style.scss";
</style>
