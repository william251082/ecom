<template>
  <div class="products-container">
    <ProductListContainer />
  </div>
</template>

<script>
// @ is an alias to /src
import ProductListContainer from "@/components/ProductListContainer.vue";

export default {
  name: "products",
  components: { ProductListContainer }
};
</script>
