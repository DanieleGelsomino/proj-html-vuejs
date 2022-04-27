<template>
  <div class="dg-bg-blog pt-5">
    <div class="d-flex flex-column align-items-center">
      <span class="text-uppercase">tales from the barber shop</span>
      <h2>Recent Blog Posts</h2>
    </div>
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
    <div class="d-flex justify-content-center pt-3 pb-5">
      <button class="dg-btn text-uppercase">read more from our blog</button>
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
    };
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
</style>