<template>
  <div>
    <div
      class="
        dg-bg-footer
        d-flex
        align-items-center
        justify-content-evenly
        pt-4
        pb-5
      "
    >
      <div class="d-flex flex-column">
        <img
          src="@/assets/img/avadabarbers_footer_shop_image-300x234.png"
          alt=""
        />
        <div class="d-flex justify-content-center pt-3 pb-5">
          <button class="dg-btn text-uppercase">Shop our range now</button>
        </div>
      </div>
      <div class="d-flex flex-column">
        <img
          class="dg-logo pb-3"
          src="@/assets/img/avadabarbers-logo-x1.png"
          alt=""
        />
        <div class="d-flex flex-column justify-content-center pt-3 pb-5">
          <ul class="ps-0">
            <li>Avada Barbers</li>
            <li>123 New York Street</li>
            <li>New York City</li>
            <li>info@yourwebsite.com</li>
            <li>+1(555)555-1212</li>
          </ul>
          <div>
            <p class="text-uppercase text-center pt-3">follow us</p>
            <div class="d-flex justify-content-evenly text-white">
              <a href="#"><i class="fa-brands fa-facebook-f"></i></a>
              <a href="#"><i class="fa-brands fa-twitter"></i></a>
              <a href="#"><i class="fa-brands fa-youtube"></i></a>
              <a href="#"><i class="fa-brands fa-instagram"></i></a>
            </div>
          </div>
        </div>
      </div>
      <div class="d-flex flex-column">
        <img
          src="@/assets/img/avadabarbers_footer_appointment_image-300x234.png"
          alt=""
        />
        <div class="d-flex justify-content-center pt-3 pb-5">
          <button class="dg-btn text-uppercase">book your appointment</button>
        </div>
      </div>
    </div>
    <div class="copyright">
      <span>
        &copy; Copyright 2012-2022 | Avada Theme by ThemeFufion | All Rights
        Reserved by Wordpress
      </span>
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
  img {
    width: 250px;
  }

  .dg-logo {
    width: 150px;
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
    text-align: center;
  }

  p {
    color: $gold;
    font-size: $fs-06;
    font-weight: $fw-700;
  }

  a {
    color: $gray;
    &:hover {
      color: $gold;
    }
  }
}

.copyright {
  background-color: #181818;
  padding: 25px;
  color: $gray;
  font-size: $fs-07;
  font-weight: $fw-300;
  display: flex;
  align-items: center;
  justify-content: center;
}
</style>