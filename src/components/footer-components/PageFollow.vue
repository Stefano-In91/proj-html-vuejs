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
      <div class="column-between">
        <img class="logo" :src="logo_img" alt="logo" />
        <ul>
          <li v-for="detail in avada_details">
            <p>{{ detail }}</p>
          </li>
        </ul>
        <div>
          <h4>Follow Us</h4>
          <div class="socials">
            <a><i class="fa-brands fa-facebook-f"></i></a>
            <a><i class="fa-brands fa-twitter"></i></a>
            <a><i class="fa-brands fa-instagram"></i></a>
            <a><i class="fa-brands fa-youtube"></i></a>
          </div>
        </div>
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
  position: relative;
  bottom: -1px;
  background-color: var(--darkbg-color);
  padding: 2rem 0 3rem;
  img:not(.logo) {
    height: 400px;
    width: 300px;
    object-fit: cover;
  }
  .column-between {
    height: 450px;
    .logo {
      width: 200px;
    }
    h4 {
      margin-bottom: 1rem;
    }
    .socials a {
      color: var(--gray-color);
      font-size: 1.25rem;
      &:not(:last-of-type) {
        margin-right: 0.5rem;
      }
    }
  }
}
</style>
