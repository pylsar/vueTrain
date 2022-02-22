<template>
  <div id="app">
    <HomePage />
    <main></main>
  </div>
</template>

<script>
import HomePage from "./views/HomePage";

export default {
  name: "App",
  components: {
    HomePage,
  },
};
</script>

<style lang="scss">
* {
  margin: 0;
  padding: 0;
}
</style>
