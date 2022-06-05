<script setup>
import ProductCart from "../components/ProductCart.vue";
</script>

<template>
  <main class="wrapper">
    <h1>Products</h1>

    <div class="card-container">
      <ProductCart
        v-for="(product, index) in inventory.slice(0, 6)"
        :key="product.id"
        :index="index"
        :product="product"
        :addToCart="addToCart"
        class="card"
      />
    </div>
  </main>
</template>

<script>
export default {
  props: ["inventory", "addToCart"],
  components: {
    ProductCart,
  },
};
</script>
