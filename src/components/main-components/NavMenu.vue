<script>
import links from "../../assets/json/nav-items.json";

export default {
  name: "NavMenu",
  props: {
    display: Boolean,
  },
  data() {
    return {
      links,
    };
  },
};
</script>
<template>
  <nav class="text-center" :class="display ? `active` : ``">
    <ul>
      <li v-for="link in links">
        <a :href="link.link" @click="$emit(`hide`)">{{ link.name }}</a>
      </li>
    </ul>
  </nav>
</template>
<style lang="scss" scpoped>
nav {
  display: none;
  background-color: var(--darkbg-color);
  color: white;
  position: relative;
  width: 100%;
  top: 0;
  padding: 3rem 0;
  &.active {
    display: block;
  }
  li {
    font-size: 1.25rem;
    &:not(:last-of-type) {
      margin-bottom: 1rem;
    }
    &:hover {
      color: var(--gold-color);
    }
  }
}
</style>
