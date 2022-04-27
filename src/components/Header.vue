<template>
  <nav :class="{ onScroll: !view.topOfPage }">
    <div class="d-flex justify-content-center dg-bg-navbar">
      <div class="row justify-content-evenly align-items-center dg-bg-navbar">
        <img
          class="col-2 dg-head-logo"
          src="@/assets/img/avadabarbers-stickylogo-x1.png"
          alt="logo-x1-avadabarbers"
        />
        <div
          class="col-5 text-white d-flex align-items-center justify-content-end"
        >
          <i class="fa-solid fa-cart-shopping me-3 dg-cart"></i>
          <ul v-if="menuStatus" class="d-flex mb-0 me-5">
            <li v-for="link in menu" :key="link">
              <a href="#">{{ link }}</a>
            </li>
          </ul>
          <div @click="showMenuOptions">
            <button
              class="menu"
              onclick="this.classList.toggle('opened');this.setAttribute('aria-expanded', this.classList.contains('opened'))"
              aria-label="Main Menu"
            >
              <svg width="100" height="100" viewBox="0 0 100 100">
                <path
                  class="line line1"
                  d="M 20,29.000046 H 80.000231 C 80.000231,29.000046 94.498839,28.817352 94.532987,66.711331 94.543142,77.980673 90.966081,81.670246 85.259173,81.668997 79.552261,81.667751 75.000211,74.999942 75.000211,74.999942 L 25.000021,25.000058"
                />
                <path class="line line2" d="M 20,50 H 80" />
                <path
                  class="line line3"
                  d="M 20,70.999954 H 80.000231 C 80.000231,70.999954 94.498839,71.182648 94.532987,33.288669 94.543142,22.019327 90.966081,18.329754 85.259173,18.331003 79.552261,18.332249 75.000211,25.000058 75.000211,25.000058 L 25.000021,74.999942"
                />
              </svg>
            </button>
          </div>
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
      menuStatus: false,
      menu: ["HOME", "SERVICES", "SHOP", "REVIEWS", "BLOG"],
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

    showMenuOptions() {
      this.menuStatus = !this.menuStatus;
    },
  },
};
</script>

<style scoped lang="scss">
@import "@/style/varstyles";

nav {
  position: fixed;
  width: 100%;
  height: 100px;
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
      color: $gold;
    }

    ul li {
      list-style-type: none;
      font-size: $fs-07;
      margin-right: 4px;
      a {
        color: #fff;
        text-decoration: none;
        &:hover {
          color: $gold;
          text-decoration-line: underline;
          text-underline-offset: 3px;
        }
      }
    }

    .menu {
      background-color: transparent;
      border: none;
      cursor: pointer;
      display: flex;
      padding: 0;
      width: 25px;
      &:hover {
        stroke: $gold;
      }
    }
    .line {
      fill: none;
      stroke: $gold;
      stroke-width: 6;
      transition: stroke-dasharray 600ms cubic-bezier(0.4, 0, 0.2, 1),
        stroke-dashoffset 600ms cubic-bezier(0.4, 0, 0.2, 1);
    }
    .line1 {
      stroke-dasharray: 60 207;
      stroke-width: 6;
    }
    .line2 {
      stroke-dasharray: 60 60;
      stroke-width: 6;
    }
    .line3 {
      stroke-dasharray: 60 207;
      stroke-width: 6;
    }
    .opened .line1 {
      stroke-dasharray: 90 207;
      stroke-dashoffset: -134;
      stroke-width: 6;
    }
    .opened .line2 {
      stroke-dasharray: 1 60;
      stroke-dashoffset: -30;
      stroke-width: 6;
    }
    .opened .line3 {
      stroke-dasharray: 90 207;
      stroke-dashoffset: -134;
      stroke-width: 6;
    }
  }
}
</style>