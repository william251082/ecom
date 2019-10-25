<template>
  <div>
    <ul class="test-list" v-for="product in productsList" :key="product.id">
      <li class="test-list--item">
        {{ product.title }}
      </li>
    </ul>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
import axios from "axios";

@Component
class ProductListContainer extends Vue {
  public productsList: any;

  super(productsList: any) {
    this.productsList = productsList;
  }

  data() {
    return {
      productsList: []
    };
  }
  mounted() {
    axios
      .get("https://jsonplaceholder.typicode.com/todos/")
      .then(response => {
        this.productsList = [...response.data].slice(0, 10);
      })
      .catch(() => {
        // Manage the state of the application if the request
        // has failed
      });
  }
}

export default ProductListContainer;
</script>
