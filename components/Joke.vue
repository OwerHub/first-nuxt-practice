<template>
  <nuxt-link :to="'jokes/' + id">
    <div class="joke">
      <p>{{ joke }}</p>
    </div>
  </nuxt-link>
</template>

<script>
export default {
  name: "Joke",
  props: ["joke", "id"],
};
</script>

<style scoped>
.joke {
  background-color: rgb(233, 231, 231);
  box-shadow: 2px 2px 2px rgba(0, 0, 0, 0.3);
  margin: 1rem 0.5rem;
  padding: 0.5rem 1rem;
  font-size: large;
  border-radius: 0.4rem;
  color: black;
}

.joke:hover {
  background-color: rgb(158, 157, 157);
}

a {
  text-decoration: none;
}
</style>
