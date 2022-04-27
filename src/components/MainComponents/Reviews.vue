<template>
  <div class="dg-view-content">
    <div class="d-flex flex-column align-items-center">
      <span class="text-uppercase">mens grooming</span>
      <h2>Services</h2>
    </div>
  </div>
</template>

<script>
export default {
  name: "ReviewsComponent",
};
</script>

<style scoped lang="scss">
@import "@/style/varstyles";

.dg-view-content {
  padding-top: 400px;

  span {
    color: $gold;
    font-size: $fs-07;
    font-weight: $fw-700;
  }

  h2 {
    font-size: 3rem;
    color: $silver;
  }
}
</style>