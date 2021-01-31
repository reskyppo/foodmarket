<template>
  <div class="home">
    <Navbar />
    <Hero />

    <div class="row mt-4">
      <div class="col">
        <h2>Best <strong>Foods</strong></h2>
      </div>
      <div class="col">
        <router-link
          to="/foods"
          class="text-secondary text-decoration-none float-right"
        >
          See all</router-link
        >
      </div>
    </div>

    <div class="row mb-3">
      <div class="col-md-4 mt-4">
        <CardProduct />
      </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import Navbar from "@/components/Navbar.vue";
import Hero from "@/components/Hero.vue";
import CardProduct from "@/components/CardProduct.vue";
import Axios from "axios";

Axios.get("http://localhost:3000/posts")
  .then(({ data }) => console.log(data))
  .catch((err) => console.log(err));
export default {
  name: "Home",
  components: {
    CardProduct,
    Hero,
    Navbar,
  },
};
</script>
