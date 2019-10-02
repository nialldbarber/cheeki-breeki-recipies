<template>
  <div id="app">
    <Products v-bind:products="productList" />
  </div>
</template>

<script>
// Data
import products from "./utils/sample.json";
// Components
import Products from "./components/Products";
// Getters
const getProducts = products[0].products;
const getDiscount = products[0].discountPercent;

// console.log(products);

export default {
  name: "app",
  components: {
    Products
  },
  data() {
    return {
      productList: getProducts,
      discount: getDiscount
    };
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
