<script>
export default {
  name: "PageAbout",
  data() {
    return {
      bg_img: "src/assets/img/avadabarbers-about-introbackground.jpg",
    };
  },
};
</script>

<template>
  <section id="about" :style="`background-image: url(${bg_img})`">
    <div class="container flex-center">
      <div class="text-center">
        <h4>Award Winning</h4>
        <h2>Pro Barbers</h2>
        <button>Meet your new Barber</button>
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
#about {
  background-size: cover;
  position: relative;
  top: -1px;
  padding-bottom: 10rem;
}
</style>
