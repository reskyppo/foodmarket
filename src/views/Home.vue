<template>
  <div class="home">
    <Navbar />
    <Hero />
  </div>
</template>

<script>
// @ is an alias to /src
import Navbar from "@/components/Navbar.vue";
import Hero from "@/components/Hero.vue";
import Axios from "axios";

Axios.get("http://localhost:3000/posts")
  .then(({ data }) => console.log(data))
  .catch((err) => console.log(err));
export default {
  name: "Home",
  components: {
    Hero,
    Navbar,
  },
};
</script>
