<template>
  <div>
    <h3>{{ product.name }}</h3>
    <p>{{ strippedContentDesc }}</p>
  </div>
</template>

<script>
export default {
  name: "Product",
  props: ["product"],
  computed: {
    strippedContentDesc() {
      let regex = /(<([^>]+)>)/gi;
      return this.product.description.replace(regex, "");
    }
  }
};
</script>

<style>
</style>
