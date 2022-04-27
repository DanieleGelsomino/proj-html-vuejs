<template>
  <nav :class="{ onScroll: !view.topOfPage }">
    <div class="d-flex justify-content-center dg-bg-navbar">
      <div
        class="row justify-content-evenly align-items-center pt-3 dg-bg-navbar"
      >
        <img
          class="col-5 dg-head-logo"
          src="@/assets/img/avadabarbers-stickylogo-x1.png"
          alt="logo-x1-avadabarbers"
        />
        <div
          class="col-5 text-white d-flex align-items-center justify-content-end"
        >
          <i class="fa-solid fa-cart-shopping me-3 dg-cart"></i>
          <i class="fa-solid fa-bars dg-menu"></i>
        </div>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  name: "HeaderComponent",
  data() {
    return {
      view: {
        topOfPage: true,
      },
    };
  },
  beforeMount() {
    window.addEventListener("scroll", this.handleScroll);
  },
  methods: {
    handleScroll() {
      if (window.pageYOffset > 0) {
        if (this.view.topOfPage) this.view.topOfPage = false;
      } else {
        if (!this.view.topOfPage) this.view.topOfPage = true;
      }
    },
  },
};
</script>

<style scoped lang="scss">
@import "@/style/varstyles";

nav {
  position: fixed;
  width: 100%;
  height: 70px;
  background-color: transparent;
  display: flex;
  align-items: center;
  transition: all 0.2s ease-in-out;
  z-index: 99999;
  &.onScroll {
    box-shadow: 0 0 5px #aaa;
    background-color: #121413;
  }

  .dg-bg-navbar {
    position: fixed;
    top: 0;
    width: 100%;

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
}
</style>