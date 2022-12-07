<script>
export default {
  name: "PageCopyright",
  data() {
    return {
      copyright: "© Copyright 2012-2020",
      theme: "Avada Theme by InceFusion",
      rights: "All Rights Reserved",
      powered_by: "Powered by WordPress",
    };
  },
};
</script>

<template>
  <section id="copyright" class="text-center">
    <p>{{ copyright }} | {{ theme }} | {{ rights }} | {{ powered_by }}</p>
    <a href="#hero" class="go-top"><i class="fa-solid fa-circle-chevron-up"></i></a>
  </section>
</template>

<style lang="scss" scoped>
#copyright {
  padding: 3rem 0;
  background-color: var(--copyright-color);
  p {
    color: rgba(169, 169, 169, 0.185);
  }
  a.go-top {
    position: absolute;
    bottom: 0;
    right: 10%;
    padding: 0.5rem 1rem;
    color: var(--gray-color);
    background-color: var(--darkbg-color);
    border-top-left-radius: 8px;
    border-top-right-radius: 8px;
  }
}
</style>
