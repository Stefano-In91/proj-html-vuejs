<script>
import ShopCard from "../card-components/ShopCard.vue";
import FeaturedCard from "../card-components/FeaturedCard.vue";

import products from "../../assets/json/products.json";
import featuredProduct from "../../assets/json/featured-product.json";

export default {
  name: "PageShop",
  components: {
    ShopCard,
    FeaturedCard,
  },
  data() {
    return {
      products,
      featured: featuredProduct[0],
      bg_img: "src/assets/img/avadabarbers-reviewsbackground.jpg",
    };
  },
};
</script>

<template>
  <section id="page-shop" :style="`background-image: url(${bg_img})`">
    <div class="text-center">
      <h4>We have you covered</h4>
      <h2>Avada Grooming Products</h2>
      <div class="flex-center">
        <ShopCard
          v-for="product in products"
          :image="product.image"
          :name="product.name"
          :price="product.price"
        />
      </div>
      <button>Shop our product range</button>
    </div>
    <FeaturedCard
      :background="featured.featured_bg"
      :image="featured.featured_img"
      :name="featured.featured_item_name"
      :description="featured.featured_item_description"
    />
  </section>
</template>

<style lang="scss" scoped>
#page-shop {
  position: relative;
  background-size: cover;
  background-position: center;
  padding-bottom: 10rem;
  button {
    margin-top: 2rem;
  }
}
</style>
