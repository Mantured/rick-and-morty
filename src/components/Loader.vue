<template>
  <div class="loader">
    <img src="../assets/images/loader.webp" alt="images od Rick paceful" />
    <h1 class="animate__animated animate__flip">A peaceful rick</h1>
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
  img {
    width: 100%;
    height: 85vh;
  }
  h1 {
    top: 50%;
    right: 50%;
    padding: 2rem;
    position: absolute;
    border-radius: 2rem;
    filter: opacity(0.7);
    text-transform: uppercase;
    background-color: whitesmoke;
    animation-duration: 5s; /* don't forget to set a duration! */
    /* transform: translate(-50% -50%); */
  }
  //animation: animate__flip; /* referring directly to the animation's @keyframe declaration */
}
</style>
