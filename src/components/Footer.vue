<template>
  <div class="dg-bg-footer d-flex align-items-center">
    <div class="d-flex flex-column justify-content-center align-items-center">
      <img
        src="@/assets/img/avadabarbers_footer_shop_image-200x156.png"
        alt="footer-shop-image"
      />
      <button class="dg-btn text-uppercase">Shop our range now</button>
    </div>
    <div class="d-flex flex-column align-items-center">
      <img
        src="@/assets/img/avadabarbers-logo-x1.png"
        alt="avadabarbers-logo-x1"
        class="dg-logo pt-5 pb-4"
      />
      <div class="text-center">
        <ul class="ps-0">
          <li>Avada Barbers</li>
          <li>123 New York Street</li>
          <li>New York City</li>
          <li>info@yourwebsite.com</li>
          <li>+1 (555) 555-1212</li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "FooterComponent",
};
</script>

<style scoped lang="scss">
@import "@/style/varstyles";

.dg-bg-footer {
  background-color: #121413;
  min-height: 500px;

  img {
    width: 200px;
  }

  .dg-btn {
    background-color: transparent;
    border: 2px solid $gold;
    color: $gold;
    font-size: $fs-07;
    padding: 8px 10px;
    font-weight: $fw-700;
    width: 180px;
    &:hover {
      cursor: pointer;
      color: #9b7748;
      border-color: #9b7748;
    }
  }

  .dg-logo {
    width: 120px;
  }

  ul li {
    color: #505050;
    font-weight: $fw-300;
    font-size: $fs-07;
    list-style-type: none;
  }
}
</style>