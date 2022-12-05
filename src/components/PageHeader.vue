<script>
export default {
  name: "PageHeader",
};
</script>

<template>
  <header>
    <div class="flex-between-center">
      <img src="../assets/img/avadabarbers-logo-x1.png" alt="logo" />
      <div class="icons flex-center">
        <i class="fa-solid fa-cart-shopping"></i>
        <i class="fa-solid fa-bars"></i>
      </div>
    </div>
  </header>
</template>

<style lang="scss" scoped>
header {
  padding: 1rem 0;
  background-color: inherit;
  .icons {
    color: white;
    height: 100%;
    i {
      font-size: 1.25rem;
      &:last-child {
        margin-left: 1rem;
        font-size: 1.75rem;
      }
    }
  }
}
</style>
