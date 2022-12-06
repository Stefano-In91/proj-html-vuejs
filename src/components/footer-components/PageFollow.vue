<script>
import company_details from "../../assets/json/avada-details.json";
export default {
  name: "PageFollow",
  data() {
    return {
      avada_details: company_details[0],
      logo_img: "src/assets/img/avadabarbers-logo-x1.png",
      shop_img: "src/assets/img/avadabarbers_footer_shop_image.png",
      appointment_img: "src/assets/img/avadabarbers_footer_appointment_image.png",
    };
  },
};
</script>

<template>
  <section id="follow-us">
    <div class="container flex-between-center text-center">
      <div>
        <img :src="shop_img" alt="shop" />
        <button>Shop our range Now</button>
      </div>
      <div>
        <img class="logo" :src="logo_img" alt="logo" />
        <ul>
          <li v-for="detail in avada_details">
            <p>{{ detail }}</p>
          </li>
        </ul>
        <h4>Follow Us</h4>
      </div>
      <div>
        <img :src="appointment_img" alt="appointment" />
        <button>Book your Appointment</button>
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
#follow-us {
  background-color: var(--darkbg-color);
  padding: 2rem 0 3rem;
  img:not(.logo) {
    height: 400px;
    width: 300px;
    object-fit: cover;
  }
  .logo {
    margin-bottom: 3rem;
  }
  h4 {
    margin: 2rem 0;
  }
}
</style>
