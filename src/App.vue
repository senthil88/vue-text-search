<template>
  <div id="app">
    <Header/>
    <SearchText/>
  </div>
</template>

<script>
import Header from "./components/Header";
import SearchText from "./components/SearchText";

export default {
  name: "App",
  components: {
    Header,
    SearchText
  }
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
