<script>
export default {
  name: "ImgFirstCard",
  props: {
    image: String,
    name: String,
    text: String,
  },
};
</script>

<template>
  <div class="card">
    <img :src="image" :alt="name" />
    <h3>{{ name }}</h3>
    <p>
      {{ text }}
    </p>
  </div>
</template>

<style lang="scss" scoped>
.card {
  padding: 1.5rem;
  max-width: calc(100% / 3 - 2rem);
  img {
    max-height: 6.25rem;
  }
  h3 {
    margin: 1.5rem 0;
  }
}
</style>
