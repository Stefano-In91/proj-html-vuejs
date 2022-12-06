<script>
import ImgFirstCard from "../card-components/ImgFirstCard.vue";
import SectionSeparator from "../section-separator/SectionSeparator.vue";
import services from "../../assets/json/services.json";

export default {
  name: "PageServices",
  components: {
    ImgFirstCard,
    SectionSeparator,
  },
  data() {
    return {
      services,
    };
  },
};
</script>

<template>
  <section id="services">
    <SectionSeparator
      :filter="`filter: invert(99%) sepia(35%) saturate(1022%) hue-rotate(216deg) brightness(114%) contrast(100%);`"
      :position="`top`"
    />
    <div class="container text-center">
      <h4>Mens Grooming</h4>
      <h2>Services</h2>
      <div class="flex-center">
        <ImgFirstCard
          v-for="service in services"
          :image="service.image"
          :img_height="100"
          :name="service.name"
          :text="service.text"
        />
      </div>
      <button>Read about our services</button>
    </div>
  </section>
</template>

<style lang="scss" scoped>
#services {
  position: relative;
  padding-bottom: 10rem;
  .flex-center {
    margin: 2rem 0;
  }
}
</style>
