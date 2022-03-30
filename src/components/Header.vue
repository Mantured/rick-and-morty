<template>
  <nav class="navbar navbar-light bg-light pb-0">
    <a class="navbar-brand pb-0" href="#">
      <img
        class=""
        src="../assets/images/Rick-&-morty-logo.jpg"
        alt="logo about rick & morty saga"
      />
      <span>{{ msg }}</span>
    </a>
  </nav>
</template>

<script>
export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: "Header",
  props: {
    msg: String,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
img {
  width: 200px;
  height: 100%;
}
</style>
