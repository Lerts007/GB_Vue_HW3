<template>
  <div class="productDetails">
    <img src="..//assets/logo.png" alt="" />
    <p>{{ product.name }}</p>
    <p>{{ price }}</p>
    <p v-if="product.available">Available</p>
    <p v-else="product.available">Out of stock</p>
  </div>
</template>

<script>
export default {
  props: {
    product: Object,
  },
  computed: {
    price() {
      return "$" + this.product.price;
    },
  },
};
</script>

<style lang="scss" scoped>
.productDetails {
  width: 300px;
  height: 400px;
  border: 2px solid #2c3e50;
  border-radius: 5px;
}
</style>
