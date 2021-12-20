<template>
  <header class="header">
    <h1 class="title">Jokes</h1>
    <ul>
      <li>
        <nuxt-link to="/">Home</nuxt-link>
      </li>
      <li>
        <nuxt-link to="/jokes">Jokes</nuxt-link>
      </li>
      <li>
        <nuxt-link to="/about">About</nuxt-link>
      </li>
    </ul>
  </header>
</template>

<script>
export default {
  name: "AppHeader",
};
</script>

<style scoped>
.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 1rem;
  padding: 0 1rem 1rem;
  border-bottom: 1px dotted #ccc;
}

.header .title {
  font-size: 3rem;
  color: #526488;
}

.header ul {
  display: flex;
  width: 100%;
  justify-content: end;

  color: white;
  margin-right: 0.5rem;
  height: 2rem;
}

.header a {
  display: inline-block;
  background: rgb(131, 130, 130);
  color: white;
  padding: 0.3rem 2rem;
  margin-right: 1rem;
  text-align: center;
  border-radius: 0.5rem;
  text-decoration: none;
  height: 1.5rem;
  display: flex;
  align-items: center;
}

.header a:hover {
  cursor: pointer;
  background-color: cyan;
  color: black;
}
</style>
