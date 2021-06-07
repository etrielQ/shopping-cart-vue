<template>
  <div class="home">
    Home Component
    {{ items }}
    <br />
    <br />
    <div class="product-cards-container">
      <ProductSummaryCard
        v-for="product in items"
        :key="product.id"
        :product="product"
      />
    </div>
  </div>
</template>

<script>
import items from "../data/items";
import ProductSummaryCard from "../components/products/ProductSummaryCard";
export default {
  name: "Home",
  components: {
    ProductSummaryCard,
  },
  data() {
    return {
      items: items,
    };
  },
};
</script>

<style lang="scss">
.product-cards-container {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
}
</style>
