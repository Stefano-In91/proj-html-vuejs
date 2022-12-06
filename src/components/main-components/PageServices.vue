<script>
import ImgFirstCard from "../card-components/ImgFirstCard.vue";
import services from "../../assets/json/services.json";

export default {
  name: "PageServices",
  components: {
    ImgFirstCard,
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
  padding-bottom: 10rem;
  .flex-center {
    margin: 2rem 0;
  }
}
</style>
