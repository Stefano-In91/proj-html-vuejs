<script>
import PageFollow from "./footer-components/PageFollow.vue";
import PageCopyright from "./footer-components/PageCopyright.vue";

export default {
  name: "PageFooter",
  components: {
    PageFollow,
    PageCopyright,
  },
};
</script>

<template>
  <footer>
    <PageFollow />
    <PageCopyright />
  </footer>
</template>

<style lang="scss" scoped></style>
