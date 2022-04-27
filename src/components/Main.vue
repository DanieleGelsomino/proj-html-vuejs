<template>
  <div>
    <!-- ****** Awards section ****** -->
    <div
      class="
        dg-bg-awards
        d-flex
        flex-column
        align-items-center
        justify-content-center
        p-5
      "
    >
      <span class="dg-little-title text-uppercase">Award winning</span>
      <h2 class="dg-title">Pro Barbers</h2>
      <button class="dg-btn text-uppercase mt-2">Meet your new barber</button>
    </div>
    <!-- ****** White triangle svg ****** -->
    <svg
      class="fusion-big-triangle-candy dg-triangle"
      xmlns="http://www.w3.org/2000/svg"
      version="1.1"
      width="100%"
      height="70"
      viewBox="0 0 100 100"
      preserveAspectRatio="none"
      style="fill: #ffffff; padding: 0"
    >
      <path d="M0 100 L50 2 L100 100 Z"></path>
    </svg>
    <!-- ****** Services section ****** -->
    <Services />
    <!-- ****** Black Triangle svg ****** -->
    <svg
      class="fusion-big-triangle-candy dg-triangle-black"
      xmlns="http://www.w3.org/2000/svg"
      version="1.1"
      width="100%"
      height="70"
      viewBox="0 0 100 100"
      preserveAspectRatio="none"
      style="fill: #121415; padding: 0"
    >
      <path d="M0 100 L50 2 L100 100 Z"></path>
    </svg>
    <!-- ****** Products section ****** -->
    <Products />
    <!-- ****** Reviews section ****** -->
    <Reviews />
  </div>
</template>

<script>
import Services from "@/components/MainComponents/Services.vue";
import Products from "@/components/MainComponents/Products.vue";
import Reviews from "@/components/MainComponents/Reviews.vue";
export default {
  name: "MainComponent",
  components: {
    Services,
    Products,
    Reviews,
  },
};
</script>

<style scoped lang="scss">
@import "@/style/varstyles";

.dg-bg-awards {
  background-image: url("../assets/img/avadabarbers-about-introbackground.jpg");
  background-size: cover;

  .dg-little-title {
    color: $gold;
    font-size: $fs-07;
    font-weight: $fw-700;
  }

  .dg-title {
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

.dg-triangle {
  background-image: url("../assets/img/avadabarbers-about-introbackground.jpg");
  background-size: cover;
  background-position-y: 30%;
}

.dg-triangle-black {
  background-color: white;
}
</style>