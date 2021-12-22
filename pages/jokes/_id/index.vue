<template>
  <div>
    <nuxt-link to="/jokes"> Back to Jokes</nuxt-link>
    <h2>{{ joke }}</h2>

    <small class="small">Joke ID: {{ $route.params.id }}</small>
  </div>
</template>

<script>
import axios from "axios";

export default {
  data() {
    return {
      joke: "",
    };
  },
  async created() {
    const config = {
      headers: {
        Accept: "application/json",
      },
    };

    try {
      const url = `https://icanhazdadjoke.com/j/${this.$route.params.id}`;
      const res = await axios.get(url, config);

      this.joke = res.data.joke;
    } catch (error) {
      console.log(error);
    }
  },
  head() {
    return {
      title: this.joke,
      meta: [
        {
          hid: "description",
          name: "description",
          content: "Best place corny dad jokes",
        },
      ],
    };
  },
};
</script>

<style scoped>
small {
  display: block;
  padding: 0 2rem;
  text-align: right;
}
</style>
