<script>
export default {
  name: "ReviewCard",
  props: {
    image: String,
    name: String,
    text: String,
  },
};
</script>

<template>
  <div class="card">
    <p>{{ text }}</p>
    <img :src="image" :alt="name" />
    <small>{{ name }}</small>
  </div>
</template>

<style lang="scss" scoped>
.card {
  max-width: calc(100% / 3 - 1.5rem);
  padding: 2rem;

  img {
    border-radius: 100%;
    height: 8rem;
    padding: 1rem 0 0.5rem;
  }
  small {
    display: block;
    color: var(--gold-color);
    font-size: 1rem;
    font-weight: bold;
    font-style: italic;
  }
}
</style>
