<template>
  <ProductDetails
    v-for="(product, index) in products"
    :key="index"
    :product="product"
  />
</template>

<script>
import ProductDetails from "./components/ProductDetails.vue";

export default {
  name: "App",
  components: { ProductDetails },
  data() {
    return {
      products: [
        {
          name: "Phone",
          price: 99.99,
          available: false,
        },
        {
          name: "Fridge",
          price: 59.99,
          available: true,
        },
        {
          name: "Video camera",
          price: 199.0,
          available: true,
        },
        {
          name: "Hoover",
          price: 38.49,
          available: true,
        },
      ],
    };
  },
};
</script>

<style lang="scss">
#app {
  display: flex;
  flex-wrap: wrap;
  gap: 10px;
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
