<script>
import ShopCard from "../card-components/ShopCard.vue";
import products from "../../assets/json/products.json";
import featuredProduct from "../../assets/json/featured-product.json";

export default {
  name: "PageShop",
  components: {
    ShopCard,
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
    <div class="featured-product flex">
      <div class="featured-image" :style="`background-image: url(${featured.featured_bg})`">
        <img :src="featured.featured_img" :alt="featured.featured_item_name" />
      </div>
      <div class="featured-description flex-center">
        <div>
          <h4>This month's featured product</h4>
          <h2>{{ featured.featured_item_name }}</h2>
          <p>{{ featured.featured_item_description }}</p>
          <button>Buy Now</button>
        </div>
      </div>
    </div>
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
  .featured-product {
    position: absolute;
    left: 50%;
    bottom: -50%;
    transform: translate(-50%, -25%);
    border-top: 4px solid var(--gold-color);
    max-height: calc(var(--container) / 10 * 4);
    width: var(--container);
    .featured-image {
      max-width: 40%;
      background-size: cover;
      img {
        display: block;
        height: 100%;
      }
    }
    .featured-description {
      position: relative;
      left: -1px;
      max-width: 60%;
      padding: 3rem;
      background-color: var(--darkbg-color);
    }
  }
}
</style>
