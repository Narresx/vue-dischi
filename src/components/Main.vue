<template>
  <main class="background-main">
    <section class="container w-80">
      <div class="row py-5">
        <div v-for="(album, index) in albums" :key="index" class="col w-25">
          <div class="card d-flex justify-content-center background-card my-2">
            <img :src="album.poster" alt="" />
            <div class="container text-center">
              <h2 class="text-white p-2">
                {{ album.title }}
              </h2>
              <div class="text-muted">
                {{ album.author }}
              </div>
              <div class="text-muted">
                {{ album.year }}
              </div>
            </div>
          </div>
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
        this.albums = res.data.response;
      });
  },
};
</script>

<style scoped>
.background-main {
  background-color: rgb(30, 45, 59);
}

.card img {
  height: 205px;
  padding: 10px;
}

.background-card {
  background-color: rgb(46, 58, 70);
}

h2 {
  font-size: 0.9rem;
}
</style>