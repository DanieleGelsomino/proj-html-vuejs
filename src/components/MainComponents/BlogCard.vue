<template>
  <div class="d-flex flex-column align-items-center pt-4">
    <div class="img-hover-zoom">
      <img :src="require('@/assets/img/' + img + '')" alt="" />
    </div>

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

.img-hover-zoom {
  overflow: hidden;
  img {
    width: 220px;
    transition: transform 1.5s ease;
    &:hover {
      transform: scale(1.3);
    }
  }
}

h4 {
  color: $gold;
  font-weight: $fw-700;
  width: 80%;
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