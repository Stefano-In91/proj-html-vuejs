<script>
import PageHero from "./main-components/PageHero.vue";
import PageAbout from "./main-components/PageAbout.vue";
import PageServices from "./main-components/PageServices.vue";
import PageShop from "./main-components/PageShop.vue";
import PageReviews from "./main-components/PageReviews.vue";
import PageBlog from "./main-components/PageBlog.vue";

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
};
</script>

<template>
  <main>
    <PageHero />
    <PageAbout />
    <PageServices />
    <PageShop />
    <PageReviews />
    <PageBlog />
  </main>
</template>

<style lang="scss" scoped></style>
