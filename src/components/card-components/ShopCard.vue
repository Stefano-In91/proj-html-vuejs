<script>
export default {
  name: "ImgFirstCard",
  props: {
    image: String,
    name: String,
    price: String,
  },
};
</script>

<template>
  <div class="card">
    <img :src="image" :alt="name" />
    <h3>{{ name }}</h3>
    <p>
      {{ price }}
    </p>
  </div>
</template>

<style lang="scss" scoped>
.card {
  padding: 1.5rem;
  max-width: calc(100% / 4 - 2rem);
  img {
    max-height: 25rem;
    max-width: 100%;
  }
  h3 {
    margin: 1.5rem 0;
  }
  p {
    color: var(--gold-color);
  }
}
</style>
