<template>
  <div class="card" style="width: 18rem">
    <img :src="rickChild.image" class="card-img-top" alt="" />
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
/*  */
</style>
