<script setup>
import ProductCart from "../components/ProductCart.vue";
</script>

<template>
  <div class="home">
    <div class="splash-container">
      <div class="splash">
        <h1>Splendid Food</h1>
      </div>
    </div>

    <main class="wrapper">
      <h2>Recommended</h2>

      <div class="recommended">
        <ProductCart
          v-for="(product, index) in inventory.slice(0, 3)"
          :key="product.id"
          :index="index"
          :product="product"
          :addToCart="addToCart"
          class="card"
        />
      </div>
    </main>
  </div>
</template>

<script>
export default {
  name: "HomeView",
  props: ["inventory", "addToCart"],
  components: {
    ProductCart,
  },
};
</script>

