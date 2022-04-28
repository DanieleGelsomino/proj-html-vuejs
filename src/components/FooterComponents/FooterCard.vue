<template>
  <div>
    <!-- ****** Footer Card with image and button ****** -->
    <div class="d-flex flex-column">
      <img :src="require('@/assets/img/' + img + '')" alt="" />

      <div class="d-flex justify-content-center pt-3 pb-5">
        <button class="dg-btn text-uppercase">{{ text_btn }}</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "FooterCard",
  props: {
    img: String,
    text_btn: String,
  },
};
</script>

<style scoped lang="scss">
@import "@/style/varstyles";

.dg-btn {
  background-color: transparent;
  border: 2px solid $gold;
  color: $gold;
  font-size: $fs-07;
  padding: 8px 20px;
  font-weight: $fw-700;
  &:hover {
    cursor: pointer;
    color: #9b7748;
    border-color: #9b7748;
  }
}
</style>