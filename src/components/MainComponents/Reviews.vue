<template>
  <div class="position-relative">
    <div class="row justify-content-center">
      <div class="col-8 dg-banner">
        <div class="row">
          <div
            class="
              col-5
              dg-bg-barber-img
              d-flex
              justify-content-center
              align-items-center
            "
          >
            <img
              src="@/assets/img/shaving_butter-200x200.png"
              alt="shaving_butter"
            />
          </div>
          <div class="col-7 dg-text-banner">
            <div class="d-flex flex-column align-items-start">
              <span class="text-uppercase">this months featured product</span>
              <h2>Shaving Butter</h2>
              <p>
                Lorem ipsum dolor sit amet consectetur adipisicing elit. Alias,
                dolorum. Molestias inventore ipsam ea voluptates nihil
                praesentium nisi excepturi aspernatur.
              </p>
              <button class="text-uppercase dg-btn">Buy now</button>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="dg-view-content">
      <div class="d-flex flex-column align-items-center">
        <span class="text-uppercase">what people say</span>
        <h2>Reviews</h2>
      </div>
      <div class="d-flex justify-content-center">
        <div class="d-flex justify-content-evenly text-center dg-w-70">
          <AboutCard
            v-for="(testimonial, index) in testimonials"
            :key="index"
            :reviews="testimonial.reviews"
            :testimonial="testimonial.testimonial"
            :profile="testimonial.profile"
          />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import AboutCard from "@/components/MainComponents/AboutCard.vue";

export default {
  name: "ReviewsComponent",
  components: {
    AboutCard,
  },
  data() {
    return {
      testimonials: [
        {
          profile: "avadabarbers-trimcut-gallery6-200x200.jpg",
          reviews:
            "Lorem ipsum dolor sit amet. consecterur adipiscind elit. Morbi mollis eleifend ante ut sagittis. Sed sodales, urna et imperdiet placerat, ex nisi aliquam orci, ac varius odio libero et arcu.",
          testimonial: "John Doe",
        },
        {
          profile: "avadabarbers-trimcut-gallery7-200x201.jpg",
          reviews:
            "Lorem ipsum dolor sit amet. consecterur adipiscind elit. Morbi mollis eleifend ante ut sagittis. Sed sodales, urna et imperdiet placerat, ex nisi aliquam orci, ac varius odio libero et arcu.",
          testimonial: "Pete Jones",
        },
        {
          profile: "avadabarbers-trimcut-gallery3-200x201.jpg",
          reviews:
            "Lorem ipsum dolor sit amet. consecterur adipiscind elit. Morbi mollis eleifend ante ut sagittis. Sed sodales, urna et imperdiet placerat, ex nisi aliquam orci, ac varius odio libero et arcu.",
          testimonial: "John Doe",
        },
      ],
    };
  },
};
</script>

<style scoped lang="scss">
@import "@/style/varstyles";

.dg-banner {
  border-top: 3px solid $gold;
  min-height: 300px;
  position: absolute;
  top: -50px;

  .dg-bg-barber-img {
    background-image: url("@/assets/img/avadabarbers-cta-background.jpg");
    background-size: cover;
  }

  .dg-text-banner {
    padding: 40px;
    background-color: #121413;
  }

  span {
    color: $gold;
    font-size: $fs-07;
    font-weight: $fw-700;
  }

  h2 {
    font-size: 2.8rem;
    color: $silver;
  }

  p {
    font-size: $fs-08;
    font-weight: $fw-300;
    color: $gray;
  }

  .dg-btn {
    background-color: transparent;
    border: 2px solid $gold;
    color: $gold;
    font-size: $fs-07;
    padding: 8px 30px;
    font-weight: $fw-700;
    &:hover {
      cursor: pointer;
      color: #9b7748;
      border-color: #9b7748;
    }
  }
}
.dg-view-content {
  padding-top: 350px;

  .dg-w-70 {
    width: $w-70;
  }

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