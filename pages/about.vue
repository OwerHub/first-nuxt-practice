<template>
  <div>
    <h1>This is About Page</h1>
    <p>this is an app that displays corny dad jokes</p>
  </div>
</template>

<script>
export default {
  head() {
    return {
      title: "About The App",
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

<style scoped></style>
