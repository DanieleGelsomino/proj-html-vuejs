<template>
  <div>
    <div class="d-flex flex-column align-items-center">
      <span class="text-uppercase">mens grooming</span>
      <h2>Services</h2>
    </div>
    <div class="d-flex justify-content-center pt-5 text-center">
      <div class="d-flex flex-column align-items-center">
        <img
          src="@/assets/img/avadabarbers-trimcut-icon-before.png"
          alt="trimcut-icon"
        />
        <h4>Trim & cut</h4>
        <p>
          Avada Barbers are experts in the lickety split trim and hair aut.
          Quick but careful and ridiculously good looking.
        </p>
      </div>
      <div class="d-flex flex-column align-items-center">
        <img
          src="@/assets/img/avadabarbers-washndry-icon.png"
          alt="washndry-icon"
        />
        <h4>Wash & Dry</h4>
        <p>
          Take a seat in our fine leather chairs. lean back and let us lather
          you a fresh head in a luxurious fashion
        </p>
      </div>
      <div class="d-flex flex-column align-items-center">
        <img
          src="@/assets/img/avadabarbers-beardtrim-icon.png"
          alt="washndry-icon"
        />
        <h4>Beard Tidy</h4>
        <p>
          Tame the tangles and untidy facial hairs like a gentleman with our
          Beard Tidy services from Avada Barbers.
        </p>
      </div>
    </div>
    <!-- ****** Button with hidden text ****** -->
    <div
      class="
        d-flex
        flex-column
        align-items-center
        justify-content-center
        pt-3
        pb-5
      "
    >
      <div>
        <button @click="showMoreText" class="dg-btn text-uppercase">
          Read about our services
        </button>
      </div>
      <p v-if="showMore" class="pt-4 text-center">
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Animi quisquam
        sequi dolorem nulla? Corporis accusantium dolor repudiandae nesciunt rem
        ipsam voluptate, exercitationem temporibus ratione libero nostrum
        maiores hic cumque veritatis cupiditate, magnam officia, obcaecati
        distinctio sapiente quasi numquam illo dolorem est voluptatum. Deleniti
        nesciunt, harum repudiandae numquam, nulla ab cum laudantium aspernatur
        sint enim quibusdam alias dolore voluptatibus placeat tempore mollitia
        animi sequi corrupti quia ea, sit repellat fugit quos aut. Voluptatibus,
        itaque a. Eaque nisi doloremque vero error a.
      </p>
    </div>
  </div>
</template>

<script>
export default {
  name: "ServicesComponent",
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

span {
  color: $gold;
  font-size: $fs-07;
  font-weight: $fw-700;
}

h2 {
  font-size: 3rem;
  color: $silver;
}

img {
  width: 50px;
  height: 80px;
  margin-bottom: 20px;
}

h4 {
  color: $gold;
  font-weight: $fw-700;
}

p {
  font-size: $fs-08;
  width: 50%;
  font-weight: $fw-300;
  color: $gray;
}

.dg-btn {
  background-color: transparent;
  border: 2px solid $gold;
  color: $gold;
  font-size: 0.7rem;
  padding: 8px 18px;
  font-weight: $fw-700;
  &:hover {
    cursor: pointer;
    color: #fff;
    background-color: $gold;
    outline: 2px solid $gold;
    outline-offset: 1px;
  }
}
</style>