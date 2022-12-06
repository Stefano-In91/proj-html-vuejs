<script>
export default {
  name: "SectionSeparator",
  props: {
    filter: String,
    position: String,
  },
  data() {
    return {
      separator: "src/assets/img/section-separator.png",
    };
  },
};
</script>
<template>
  <img
    :src="separator"
    :style="`${filter} ${position}:-99px;`"
    :class="position === `top` ? `` : `rotated`"
  />
</template>
<style lang="scss" scoped>
img {
  position: absolute;
  width: 100%;
  height: 100px;
  background-color: transparent;
  &.rotated {
    transform: rotate(180deg);
  }
}
</style>
