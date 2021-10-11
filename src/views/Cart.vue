<template>
  <div>
    <h1>
      Yout Cart
    </h1>
    <CartItemCard
      v-for="product in products"
      :key="product.id"
      :product="product"
    />
    <CartSummaryPaymentCard />
  </div>
</template>
<script>
import CartItemCard from "../components/Cart/CartItemCard";
import CartSummaryPaymentCard from "../components/Cart/CartSummaryPaymentCard.vue";
export default {
  components: {
    CartItemCard,
    CartSummaryPaymentCard,
  },
  computed: {
    products() {
      return this.$store.getters.cartItems;
    },
  },
};
</script>
