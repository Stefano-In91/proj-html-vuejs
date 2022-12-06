<script>
import ImgFirstCard from "../card-components/ImgFirstCard.vue";

import blog_posts from "../../assets/json/blog-posts.json";

export default {
  name: "PageBlog",
  components: {
    ImgFirstCard,
  },
  data() {
    return {
      blog_posts,
    };
  },
};
</script>

<template>
  <section id="blog" class="text-center">
    <h4>Tales from the barber shop</h4>
    <h2>Recent Blog Posts</h2>
    <div class="container flex-between-center">
      <ImgFirstCard
        v-for="post in blog_posts"
        :image="post.image"
        :img_height="150"
        :name="post.name"
        :text="post.text"
      />
    </div>
    <button>Read more from our Blog</button>
  </section>
</template>

<style lang="scss" scoped>
#blog {
  background-color: var(--lightbg-color);
  padding-top: 10rem;
  .container {
    padding: 2rem 0;
  }
}
</style>
