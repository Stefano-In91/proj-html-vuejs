<script>
import NavMenu from "./main-components/NavMenu.vue";

export default {
  name: "PageHeader",
  components: {
    NavMenu,
  },
  data() {
    return {
      showNav: false,
    };
  },
  methods: {
    toggleNavbar() {
      this.showNav = !this.showNav;
    },
  },
};
</script>

<template>
  <header :class="showNav ? `navActive` : ``">
    <div class="container">
      <div class="flex-between-center">
        <img src="../assets/img/avadabarbers-logo-x1.png" alt="logo" />
        <div class="icons flex-center">
          <a><i class="fa-solid fa-cart-shopping"></i></a>
          <a @click="toggleNavbar"><i class="fa-solid fa-bars"></i></a>
        </div>
      </div>
    </div>
    <NavMenu :display="showNav" @hide="toggleNavbar" />
  </header>
</template>

<style lang="scss" scoped>
header {
  position: absolute;
  z-index: 99;
  padding: 1rem 0;
  background-color: inherit;
  &.navActive {
    background-color: var(--darkbg-color);
  }
  .icons {
    color: white;
    height: 100%;
    a {
      font-size: 1.25rem;
      &:last-child {
        margin-left: 1rem;
        font-size: 1.75rem;
      }
    }
  }
}
</style>
