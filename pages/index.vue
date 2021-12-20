<template>
  <div>
    Hello Nuxt!
    <!--  <Tutorial /> -->
  </div>
</template>

<script>
export default {
  name: "IndexPage",
  head() {
    return {
      title: "Welcome to DadJokes",

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
