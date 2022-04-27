<template>
  <div class="d-flex flex-column align-items-center pt-4">
    <img :src="require('@/assets/img/' + img + '')" alt="" />
    <h4>{{ title }}</h4>
    <p>{{ text }}</p>
  </div>
</template>

<script>
export default {
  name: "BlogCard",
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
  width: 220px;
}

h4 {
  color: $gold;
  font-weight: $fw-700;
  width: 90%;
  text-align: center;
  padding-top: 10px;
}

p {
  font-size: $fs-08;
  width: 90%;
  text-align: center;
  font-weight: $fw-300;
  color: $gray;
}
</style>