<template>
  <div class="d-flex justify-content-center dg-bg">
    <div class="row justify-content-between align-items-center dg-w-70">
      <div class="col-6">
        <h1 class="text-white title">Barber Shop</h1>
        <div class="dg-line"></div>
        <p class="dg-text pt-3">The Pinnacle of Male Grooming</p>
        <button class="dg-btn text-uppercase mt-2">learn more</button>
      </div>
      <div class="col-6 d-flex justify-content-end pt-5 pb-5">
        <img
          src="@/assets/img/avadabarbers_hero_focalmirror-400x550.png"
          alt="avadabarbers_hero_focalmirror"
        />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "JumbotronComponent",
};
</script>

<style scoped lang="scss">
@import "@/style/varstyles";

.dg-bg {
  background-image: url("../assets/img/avadabarbers-homepage-hero-bg.jpg");
  background-size: cover;
  .dg-w-70 {
    width: $w-70;
  }

  .title {
    font-size: 3.2rem;
  }

  .dg-line {
    height: 3px;
    width: 125px;
    background-color: $gold;
  }

  .dg-text {
    color: #505050;
    font-weight: $fw-300;
  }

  .dg-btn {
    background-color: transparent;
    border: 2px solid $gold;
    color: $gold;
    font-size: 0.7rem;
    padding: 5px 18px;
    font-weight: $fw-700;
  }
}
</style>