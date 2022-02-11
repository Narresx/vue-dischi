<template>
  <header class="p-3 d-flex justify-content-around align-items-center">
    <img
      src="https://www.nicepng.com/png/full/811-8110513_spotify-logo-spotify.png"
    />
    <Search />
  </header>
</template>

<script>
import Search from "./Search.vue";
export default {
  name: "Header",
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