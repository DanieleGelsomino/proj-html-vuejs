<template>
  <div class="d-flex justify-content-center dg-bg p-3">
    <div class="row justify-content-between align-items-center dg-w-70">
      <div class="col-6">
        <h1 class="dg-title">Barber Shop</h1>
        <div class="dg-line"></div>
        <p class="dg-text pt-3">The Pinnacle of Male Grooming</p>
        <!-- ****** Button with hidden text ****** -->
        <button @click="showMoreText" class="dg-btn text-uppercase mt-2">
          learn more
        </button>
        <p v-if="showMore" class="dg-text dg-w-80 pt-3">
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Perferendis,
          recusandae. Numquam tempora facere reprehenderit odio dolore obcaecati
          fugit temporibus neque, inventore possimus sed, nam earum quibusdam?
          Nihil iste eum iure?
        </p>
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
  data() {
    return {
      showMore: false,
    };
  },

  methods: {
    showMoreText() {
      this.showMore = !this.showMore;
    },
  },
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

  .dg-title {
    font-size: 3.2rem;
    color: $silver;
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
    padding: 8px 20px;
    font-weight: $fw-700;
    &:hover {
      cursor: pointer;
      color: #9b7748;
      border-color: #9b7748;
    }
  }

  .dg-w-80 {
    width: $w-80;
  }

  p {
    transition-delay: 2s;
  }
}
</style>