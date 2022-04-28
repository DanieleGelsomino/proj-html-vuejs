<template>
  <div>
    <!-- <img :src="require('@/assets/img/' + img + '')" alt="" />
    <h4>{{ product_name }}</h4>
    <p>{{ price }}</p> -->
    <div class="d-flex flex-column align-items-center">
      <img :src="require('@/assets/img/' + img + '')" alt="" />
      <h4>{{ title }}</h4>
      <p>{{ text }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "ProductCard",
  props: {
    img: String,
    title: String,
    text: String,
  },
};
</script>

<style scoped lang="scss">
@import "@/style/varstyles";

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
</style>