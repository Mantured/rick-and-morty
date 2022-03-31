<template>
  <div class="card p-3 mb-5 rounded-pill">
    <img :src="image" class="card-img-top p-2 rounded-pill" alt="" />
    <div class="card-body text-center">
      <h5 class="card-title my-size text-white bg-dark p-1 rounded fw-bold">
        {{ title }}
      </h5>
      <p class="card-text text-secondary">
        status: <span class="text-warning"> {{ description }} </span>
      </p>
      <p class="card-text fw-bold">{{ boldDescription }}</p>
    </div>
  </div>
</template>

<script>
export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: "Citizen",
  props: ["title", "image", "description", "boldDescription"],
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
  div h5 {
    filter: opacity(0.8);
  }
}
</style>
