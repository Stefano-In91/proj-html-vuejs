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
  </section>
</template>

<style lang="scss" scoped>
#copyright {
  padding: 3rem 0;
  background-color: var(--copyright-color);
  p {
    color: rgba(169, 169, 169, 0.185);
  }
}
</style>
