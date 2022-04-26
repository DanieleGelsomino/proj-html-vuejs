<template>
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
  <!-- ****** Service section ****** -->
</template>

<script>
export default {
  name: "MainComponent",
};
</script>

<style scoped lang="scss">
@import "@/style/varstyles";

.dg-bg-awards {
  background-image: url("../assets/img/avadabarbers-about-introbackground.jpg");
  background-size: cover;

  .dg-little-title {
    color: $gold;
    font-size: 0.7rem;
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
    font-size: 0.7rem;
    padding: 5px 18px;
    font-weight: $fw-700;
    &:hover {
      cursor: pointer;
    }
  }
}
</style>