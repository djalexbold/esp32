<template>
  <div id="app">
    <header>
      <NavBar />
    </header>
    <main>
      <AppMain />
    </main>
    <AppFooter />
  </div>
</template>

<script>
import NavBar from "./components/NavBar.vue";
import AppFooter from "./components/AppFooter.vue";
import AppMain from "./components/AppMain.vue";

export default {
  name: 'App',
  components: {
    NavBar,
    AppMain,
    AppFooter,
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  margin: auto;
  color: #2c3e50;
  background-color: #fafafa;
}

</style>
