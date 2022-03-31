<template>
  <div class="loader">
    <img src="../assets/images/loader.webp" alt="images od Rick paceful" />
    <img
      src="../assets/images/loader-2.png"
      class="animate__animated animate__heartBeat rounded-circle"
    />
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
  .animate__animated {
    width: 200px;
    height: 200px;
    top: 50%;
    right: 50%;
    padding: 0.5rem;
    position: absolute;
    filter: opacity(0.7);
    text-transform: uppercase;
    background-color: whitesmoke;
    animation-duration: 10s; /* don't forget to set a duration! */
    transform: translate(-50% -50%);
  }
  //animation: animate__flip; /* referring directly to the animation's @keyframe declaration */
}
</style>
