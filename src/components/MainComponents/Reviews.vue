<template>
  <div class="dg-view-content">
    <div class="d-flex flex-column align-items-center">
      <span class="text-uppercase">what people say</span>
      <h2>Reviews</h2>
    </div>
    <div class="d-flex justify-content-evenly text-center">
      <AboutCard
        v-for="(testimonial, index) in testimonials"
        :key="index"
        :reviews="testimonial.reviews"
        :testimonial="testimonial.testimonial"
        :profile="testimonial.profile"
      />
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