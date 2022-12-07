<script>
import DiscountCards from "../card-components/DiscountCards.vue";

export default {
  name: "PageHero",
  components: {
    DiscountCards,
  },
  props: {
    bg_img: String,
    hero_img: String,
  },
};
</script>

<template>
  <section id="hero" :style="`background-image: url(${bg_img})`">
    <div class="container flex-between-center">
      <div class="barber-shop">
        <h1>Barber Shop</h1>
        <hr />
        <p>The Pinnacle of Male Grooming</p>
        <button>Learn More</button>
      </div>
      <img :src="hero_img" alt="hero" />
    </div>
    <DiscountCards />
  </section>
</template>

<style lang="scss" scoped>
#hero {
  background-position: center;
  background-size: cover;
  h1 {
    color: white;
    font-size: 4rem;
  }
  p {
    font-size: 1.5rem;
    margin-bottom: 1.5rem;
  }
  hr {
    width: 60%;
    border: 2px solid;
    border-color: var(--gold-color);
    margin: 1.5rem 0;
  }
  img {
    height: 700px;
  }
}
</style>
