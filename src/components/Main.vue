<template>
  <main class="background-main">
    <section class="container w-80">
      <div class="row">
        <div v-for="(album, index) in albums" :key="index" class="col-2">
          {{ album.response.title }}
        </div>
      </div>
    </section>
  </main>
</template>

<script>
import axios from "axios";
export default {
  name: "Main",

  data() {
    return {
      albums: [],
    };
  },

  mounted() {
    axios
      .get("https://flynn.boolean.careers/exercises/api/array/music")
      .then((res) => {
        this.albums = res.data.results;
      });
  },
};
</script>

<style scoped>
.background-main {
  background-color: rgb(30, 45, 59);
}
</style>