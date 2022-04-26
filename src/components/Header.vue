<template>
  <div class="">
    <div class="d-flex justify-content-center dg-bg-navbar">
      <div
        class="
          row
          justify-content-between
          align-items-center
          pt-3
          dg-w-70 dg-bg-navbar
        "
      >
        <img
          class="col-2 dg-head-logo"
          src="@/assets/img/avadabarbers-stickylogo-x1.png"
          alt="logo-x1-avadabarbers"
        />
        <div
          class="col-2 text-white d-flex align-items-center justify-content-end"
        >
          <i class="fa-solid fa-cart-shopping me-3 dg-cart"></i>
          <i class="fa-solid fa-bars dg-menu"></i>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "HeaderComponent",
};
</script>

<style scoped lang="scss">
@import "@/style/varstyles";
.dg-bg-navbar {
  position: fixed;
  top: 0;
  left: 160px;
  .dg-w-70 {
    width: $w-70;
  }

  .dg-head-logo {
    width: 140px;
  }

  .dg-cart {
    font-size: 0.6rem;
  }

  .dg-cart:hover,
  .dg-menu:hover {
    cursor: pointer;
  }
}
</style>