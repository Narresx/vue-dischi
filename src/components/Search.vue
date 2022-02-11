<template>
  <div class="d-flex">
    <select
      v-model="resultSearch"
      class="form-select"
      id="music-filter"
      @change="getChoise"
    >
      <option value="All" selected>Tutti</option>
      <option value="Rock">Rock</option>
      <option value="Pop">Pop</option>
      <option value="Metal">Metal</option>
      <option value="Jazz">Jazz</option>
    </select>
  </div>
</template>

<script>
export default {
  name: "Search",

  data() {
    return {
      resultSearch: "All",
    };
  },

  methods: {
    getChoise() {
      this.$emit("searchValue", this.resultSearch);
    },
  },
};
</script>

<style>
</style>