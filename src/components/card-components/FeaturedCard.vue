<script>
export default {
  name: "FeaturedCard",
  props: {
    image: String,
    background: String,
    name: String,
    description: String,
  },
};
</script>

<template>
  <div class="featured flex">
    <div class="featured-image" :style="`background-image: url(${background})`">
      <img :src="image" :alt="name" />
    </div>
    <div class="featured-description flex-center">
      <div>
        <h4>This month's featured product</h4>
        <h2>{{ name }}</h2>
        <p>{{ description }}</p>
        <button>Buy Now</button>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.featured {
  position: absolute;
  left: 50%;
  bottom: -50%;
  transform: translate(-50%, -30%);
  border-top: 4px solid var(--gold-color);
  max-height: calc(var(--container) * 0.4);
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
</style>
