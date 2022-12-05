<script>
import PageHero from "./main-components/PageHero.vue";
import PageAbout from "./main-components/PageAbout.vue";
import PageServices from "./main-components/PageServices.vue";
import PageShop from "./main-components/PageShop.vue";
import PageReviews from "./main-components/PageReviews.vue";
import PageBlog from "./main-components/PageBlog.vue";

import heroImgs from "../assets/json/hero.json";

export default {
  name: "PageMain",
  components: {
    PageHero,
    PageAbout,
    PageServices,
    PageShop,
    PageReviews,
    PageBlog,
  },
  data() {
    return {
      heroImg: heroImgs[0],
    };
  },
};
</script>

<template>
  <main>
    <PageHero :bg_img="heroImg.hero_bg_image" :hero_img="heroImg.hero_image" />
    <PageAbout />
    <PageServices />
    <PageShop />
    <PageReviews />
    <PageBlog />
  </main>
</template>

<style lang="scss" scoped></style>
