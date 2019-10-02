<template>
  <div>
    <div v-for="product in products" v-bind:key="product.id">
      <Product v-bind:product="product" />
    </div>
  </div>
</template>

<script>
import Product from "./Product";

export default {
  name: "Products",
  props: ["products"],
  components: {
    Product
  }
};
</script>

<style>
</style>
