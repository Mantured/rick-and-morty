<template>
  <div id="app">
    <Header msg="Rick & Morty Ricklantide" />
    <Ricklantide />
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Ricklantide from "./components/Ricklantide.vue";

export default {
  name: "App",
  components: {
    Header,
    Ricklantide,
  },
};
</script>

<style lang="scss">
@import "./assets/scss/style.scss";
#app {
  position: relative;
  background-color: rgb(3, 55, 55);
}
</style>
