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
      <FooterCard
        v-for="(element, index) in buttonImg1"
        :key="index.id"
        :img="element.img"
        :text_btn="element.text_btn"
      />
      <FooterContacts />
      <FooterCard
        v-for="(element, index) in buttonImg2"
        :key="index.id"
        :img="element.img"
        :text_btn="element.text_btn"
      />
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
import FooterCard from "@/components/FooterComponents/FooterCard.vue";
import FooterContacts from "@/components/FooterComponents/FooterContacts.vue";
export default {
  name: "FooterComponent",
  components: {
    FooterCard,
    FooterContacts,
  },
  data() {
    return {
      buttonImg1: [
        {
          id: 1,
          img: "avadabarbers_footer_shop_image-300x234.png",
          text_btn: "shop our range now",
        },
      ],

      buttonImg2: [
        {
          id: 2,
          img: "avadabarbers_footer_appointment_image-300x234.png",
          text_btn: "book your appointment",
        },
      ],
    };
  },
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