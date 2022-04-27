<template>
  <div>
    <img :src="require('@/assets/img/' + img + '')" alt="" />
    <h4>{{ product_name }}</h4>
    <p>{{ price }}</p>
  </div>
</template>

<script>
export default {
  name: "ProductCard",
  props: {
    img: String,
    product_name: String,
    price: String,
  },
};
</script>

<style scoped lang="scss">
@import "@/style/varstyles";
* {
  cursor: pointer;
  &:hover {
    transition: transform 0.7s ease;
    transform: scale(1.1);
  }
}
h4 {
  color: $gold;
  font-weight: $fw-700;
  &:hover {
    transform: scale(1.1);
  }
}

p {
  font-size: $fs-08;
  width: 90%;
  font-weight: $fw-300;
  color: $gold;
  &:hover {
    transform: scale(1.1);
  }
}
</style>