<template>
  <div class="d-flex flex-column align-items-center pt-4">
    <p>{{ reviews }}</p>
    <img :src="require('@/assets/img/' + profile + '')" alt="" />
    <p class="dg-name-testimonial pt-3">{{ testimonial }}</p>
  </div>
</template>

<script>
export default {
  name: "AboutCard",
  props: {
    profile: String,
    testimonial: String,
    reviews: String,
  },
};
</script>

<style scoped lang="scss">
@import "@/style/varstyles";

p {
  font-size: $fs-08;
  width: 80%;
  font-weight: $fw-300;
  color: $gray;
}

img {
  border-radius: 50%;
  width: 100px;
}

.dg-name-testimonial {
  color: $gold;
  font-size: $fs-08;
  font-weight: $fw-700;
}
</style>