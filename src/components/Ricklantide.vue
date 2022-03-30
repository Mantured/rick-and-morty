<template>
  <main>
    <div class="container-fluid p-5">
      <div class="row" v-if="rickChildren">
        <div
          class="col-12 cols-xm-6 col-md-4 col-lg-2"
          v-for="rick in rickChildren"
          :key="rick.id"
        >
          <Citizen :rickChild="rick" />
        </div>
        <div class="col-12">
          <button
            class="btn-lg btn-warning"
            @click="getRickElement(apiRickNextAddress)"
          >
            Next
          </button>
          <!-- <button
            class="btn-lg btn-warning"
            @click="getRickElement(apiRickBackAddress)"
          >
            Back Rick Back!
          </button> -->
        </div>
      </div>
      <div class="row" v-else>
        <div class="col-12">
          <Loader />
        </div>
      </div>
    </div>
  </main>
</template>

<script>
//import axios
import axios from "axios";
import Citizen from "./Citizens.vue";
import Loader from "./Loader.vue";

export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: "Ricklantide",
  components: {
    Citizen,
    Loader,
  },
  data: function () {
    return {
      apiRickAddress: "http://rickandmortyapi.com/api/character",
      apiRickNextAddress: "",
      /* apiRickBackAddress: null, */
      rickChildren: null,
    };
  },
  created: function () {
    setTimeout(this.getRickElement, 500000, this.apiRickAddress);
  },
  methods: {
    getRickElement(apiUrl) {
      axios
        .get(apiUrl)
        .then((result) => {
          this.rickChildren = result.data.results;
          this.apiRickNextAddress = result.data.info.next;
          //this.apiRickBackAddress = result.data.info.prev;
          //console.log(result.data.info.prev);
          console.log(this.rickChildren);
        })
        .catch((error) => {
          console.warn(error);
        });
    },
  },
};
</script>

<style lang="scss" scoped>
/*  */
</style>
