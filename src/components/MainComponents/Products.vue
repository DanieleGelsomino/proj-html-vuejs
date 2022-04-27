<template>
  <div class="dg-bg-products d-flex flex-column pb-5">
    <div class="d-flex flex-column align-items-center pt-5">
      <span class="text-uppercase">we have you covered</span>
      <h2>Avada Grooming Products</h2>
    </div>
    <div class="pt-3">
      <div class="d-flex justify-content-evenly text-center">
        <ProductCard
          v-for="(item, index) in products"
          :key="index"
          :img="item.img"
          :product_name="item.product_name"
          :price="item.price"
        />
      </div>
      <div class="d-flex justify-content-center pt-3 pb-5">
        <button class="dg-btn text-uppercase">Shop our product range</button>
      </div>
    </div>
  </div>
</template>

<script>
import ProductCard from "@/components/MainComponents/ProductCard.vue";
export default {
  name: "ProductsComponent",
  components: {
    ProductCard,
  },
  data() {
    return {
      products: [
        {
          img: "brush_dark-200x200.png",
          product_name: "Brush",
          price: "$15.00",
        },
        {
          img: "scissors-200x200.png",
          product_name: "Scissors",
          price: "$85.00",
        },
        {
          img: "hot_oil_dark-200x200.png",
          product_name: "Hot Oil",
          price: "$15.00",
        },
        {
          img: "straight_razor_dark-200x200.png",
          product_name: "Straight Razor",
          price: "$30.00",
        },
      ],
    };
  },
};
</script>

<style scoped lang="scss">
@import "@/style/varstyles";

.dg-bg-products {
  background-image: url("@/assets/img/avadabarbers-reviewsbackground.jpg");
  min-height: 500px;
  background-size: cover;

  span {
    color: $gold;
    font-size: $fs-07;
    font-weight: $fw-700;
  }

  h2 {
    font-size: 3rem;
    color: $silver;
  }

  .dg-btn {
    background-color: transparent;
    border: 2px solid $gold;
    color: $gold;
    font-size: $fs-07;
    padding: 8px 20px;
    font-weight: $fw-700;
    &:hover {
      cursor: pointer;
      color: #9b7748;
      border-color: #9b7748;
    }
  }
}
</style>