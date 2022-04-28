<template>
  <div class="dg-bg-blog pt-5 pb-5">
    <!-- ****** Title section ****** -->
    <div class="d-flex flex-column align-items-center">
      <span class="text-uppercase">tales from the barber shop</span>
      <h2>Recent Blog Posts</h2>
    </div>
    <!-- ****** Blog Card with img and text ****** -->
    <div class="d-flex justify-content-center">
      <div class="d-flex dg-w-70">
        <BlogCard
          v-for="(post, index) in posts"
          :key="index"
          :img="post.img"
          :title="post.title"
          :text="post.text"
        />
      </div>
    </div>
    <!-- ****** Button with hidden text ****** -->
    <div
      class="
        d-flex
        flex-column
        align-items-center
        justify-content-center
        pt-4
        pb-5
      "
    >
      <button @click="showMoreText" class="dg-btn text-uppercase">
        read more from our blog
      </button>
      <p v-if="showMore" class="pt-4 text-center">
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Vero nostrum
        cupiditate delectus fugit iure qui cum dolor velit repellat
        exercitationem? Sunt odit iste autem repellat ea laboriosam, dolor harum
        deleniti! Non saepe neque natus veritatis, eum architecto nostrum quas
        sit ea officia reiciendis, voluptatem exercitationem amet aut, dicta
        quam placeat eius. Facilis quos ut numquam perspiciatis id rerum, hic
        adipisci magnam earum est perferendis qui molestiae natus quis veniam
        provident debitis dolorem? Dolor fuga, vero ad mollitia voluptatibus
        nihil consequatur eaque ab id reprehenderit incidunt velit consectetur
        nisi obcaecati atque vitae ipsum, cumque et sint, natus illo! Eos
        perspiciatis eligendi voluptatum, aut corporis iure architecto
        doloribus, saepe iusto optio, cupiditate expedita ex sint numquam
        obcaecati enim temporibus sunt dicta sed. Voluptatum delectus eum minus
        temporibus tenetur, quasi voluptatibus reprehenderit fuga praesentium
        consequuntur. Enim rerum tenetur aliquam voluptatem itaque cum fuga
        doloremque iusto ducimus suscipit culpa molestiae, similique praesentium
        beatae voluptas!
      </p>
    </div>
  </div>
</template>

<script>
import BlogCard from "@/components/MainComponents/BlogCard.vue";

export default {
  name: "BlogComponent",
  components: {
    BlogCard,
  },
  data() {
    return {
      posts: [
        {
          img: "avadabarbers-second-blog-320x202.jpg",
          title: "Avada Barbers Now Open",
          text: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus ut dapibus magna. praesent semper.",
        },
        {
          img: "avadabarbers-choosing-blog-320x202.jpg",
          title: "Choosing The Right Barber",
          text: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus ut dapibus magna. praesent semper.",
        },
        {
          img: "avadabarbers-ourservice-blog-320x202.jpg",
          title: "Quick Service Guide",
          text: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus ut dapibus magna. praesent semper.",
        },
      ],

      showMore: false,
    };
  },
  methods: {
    showMoreText() {
      this.showMore = !this.showMore;
    },
  },
};
</script>

<style scoped lang="scss">
@import "@/style/varstyles";

.dg-bg-blog {
  background-color: $light-silver;
}

.dg-w-70 {
  width: $w-70;
}

span {
  color: $gold;
  font-size: $fs-07;
  font-weight: $fw-700;
}

h2 {
  font-size: 3rem;
  color: $silver;
}

.dg-btn {
  background-color: transparent;
  border: 2px solid $gold;
  color: $gold;
  font-size: $fs-07;
  padding: 8px 20px;
  font-weight: $fw-700;
  &:hover {
    cursor: pointer;
    color: #fff;
    background-color: $gold;
    outline: 2px solid $gold;
    outline-offset: 1px;
  }
}

p {
  font-size: $fs-08;
  width: $w-70;
  text-align: center;
  font-weight: $fw-300;
  color: $gray;
}
</style>