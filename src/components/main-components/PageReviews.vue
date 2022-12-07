<script>
import ReviewCard from "../card-components/ReviewCard.vue";
import SectionSeparator from "../section-separator/SectionSeparator.vue";

import reviews from "../../assets/json/reviews.json";

export default {
  name: "PageReviews",
  components: {
    ReviewCard,
    SectionSeparator,
  },
  data() {
    return {
      reviews,
    };
  },
};
</script>

<template>
  <section id="reviews">
    <div class="text-center">
      <h4>What people say</h4>
      <h2>Reviews</h2>
      <div class="container flex-center">
        <ReviewCard
          v-for="review in reviews"
          :image="review.thumbnail"
          :name="review.name"
          :text="review.text"
        />
      </div>
    </div>
    <SectionSeparator
      :filter="`filter: invert(94%) sepia(2%) saturate(3679%) hue-rotate(292deg) brightness(112%) contrast(110%);`"
      :position="`bottom`"
    />
  </section>
</template>

<style lang="scss" scoped>
#reviews {
  padding-top: calc(var(--container) * 0.4);
}
</style>
