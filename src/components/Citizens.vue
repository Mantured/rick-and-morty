<template>
  <div class="card p-3 mb-5 rounded-pill">
    <img :src="rickChild.image" class="card-img-top p-1 rounded-pill" alt="" />
    <div class="card-body text-center">
      <h5 class="card-title">{{ rickChild.name }}</h5>
      <p class="card-text">{{ rickChild.status }}</p>
      <p class="card-text">{{ rickChild.species }}</p>
    </div>
  </div>
</template>

<script>
export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: "Citizen",
  props: {
    rickChild: Object,
  },
};
</script>

<style lang="scss" scoped>
@import "../assets/scss/style.scss";
div.card {
  height: 400px;
  margin-bottom: 2rem;
  box-shadow: $shadow;
  img {
    width: 100%;
    height: 100%;
  }
}
</style>
