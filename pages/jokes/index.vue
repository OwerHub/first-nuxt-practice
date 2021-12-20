<template>
  <div>
    <Joke
      v-for="joke in jokes"
      :key="joke.id"
      :id="joke.id"
      :joke="joke.joke"
    ></Joke>
  </div>
</template>

<script>
import axios from "axios";
import Joke from "../../components/Joke";

export default {
  comments: { Joke },
  data() {
    return {
      jokes: [],
    };
  },

  async created() {
    const config = {
      headers: {
        Accept: "application/json",
      },
    };

    try {
      const url = "https://icanhazdadjoke.com/search";
      const res = await axios.get(url, config);

      this.jokes = res.data.results;
    } catch (error) {
      console.log(error);
    }
  },

  head() {
    return {
      title: "Dad Jokes",
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
