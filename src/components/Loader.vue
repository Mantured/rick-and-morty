<template>
  <div class="loader animate_animated animate_flip text-danger">
    <h1>Loading</h1>
  </div>
</template>

<script>
export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: "Loader",
};
</script>

<style lang="scss" scoped>
@import "../assets/scss/style.scss";
div.loader {
  //animation: animate__flip; /* referring directly to the animation's @keyframe declaration */
  //animation-duration: 10s; /* don't forget to set a duration! */
}
</style>
