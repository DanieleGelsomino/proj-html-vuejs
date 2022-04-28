<template>
  <!-- ****** Footer info contact ****** -->
  <div class="d-flex flex-column pt-4">
    <img class="dg-logo" src="@/assets/img/avadabarbers-logo-x1.png" alt="" />
    <div class="d-flex flex-column justify-content-center pt-4 pb-5">
      <ul class="ps-0">
        <li>Avada Barbers</li>
        <li>123 New York Street</li>
        <li>New York City</li>
        <li>info@yourwebsite.com</li>
        <li>+1(555)555-1212</li>
      </ul>
      <!--****** Social icons ****** -->
      <div>
        <p class="text-uppercase text-center pt-4">follow us</p>
        <div class="d-flex justify-content-evenly text-white">
          <a href="#"><i class="fa-brands fa-facebook-f"></i></a>
          <a href="#"><i class="fa-brands fa-twitter"></i></a>
          <a href="#"><i class="fa-brands fa-youtube"></i></a>
          <a href="#"><i class="fa-brands fa-instagram"></i></a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "FooterContact",
};
</script>

<style scoped lang="scss">
@import "@/style/varstyles";

.dg-logo {
  width: 120px;
}

ul li {
  color: #505050;
  font-weight: $fw-300;
  font-size: $fs-08;
  list-style-type: none;
  text-align: center;
}

p {
  color: $gold;
  font-size: $fs-07;
  font-weight: $fw-700;
}

a {
  color: $gray;
  &:hover {
    color: $gold;
  }
}
</style>