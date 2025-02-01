<template>
  <div id="app">
    <!-- Navigation -->
    <nav>
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </nav>

    <hr />

    <!-- Platzhalter für die Seiten -->
    <router-view />
  </div>
</template>

<script>
export default {
  name: 'App'
};
</script>

<style>
nav {
  background-color: #f0f0f0;
  padding: 10px;
  border-radius: 5px;
}

nav a {
  text-decoration: none;
  color: black;
  margin: 0 10px;
  font-weight: bold;
}

nav a.router-link-active {
  color: blue;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  padding: 20px;
}
</style>